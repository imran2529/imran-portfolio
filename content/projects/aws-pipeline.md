---
title: "Real-Time Event-Driven Data Pipeline"
date: 2026-03-26
description: "Architecting a high-scale Kinesis-to-Redshift streaming pipeline for a US E-commerce client."
summary: "Implemented a Medallion Architecture (Bronze-Silver-Gold) on AWS to process real-time event data with Airflow orchestration."
tags: ["AWS Kinesis", "AWS Glue", "Redshift", "Airflow", "PySpark"]
categories: ["Data Engineering", "Streaming"]
draft: false
---

## Project Overview
At **Factspan Analytics**, I architected and deployed a robust, fault-tolerant streaming pipeline for a major US-based E-commerce client. The goal was to move from batch processing to a real-time event-driven model to enable instant business insights.

### 🏗️ Architecture: The Medallion Approach
I implemented a scalable Data Lake on **Amazon S3** following the Medallion layering strategy:
* **Bronze Layer:** Raw ingestion of event streams via **AWS Kinesis Data Streams**.
* **Silver Layer:** Cleansed and validated data using **AWS Glue (PySpark)**, converted to optimized **Parquet** format.
* **Gold Layer:** Business-level aggregates and curated datasets ready for high-level analytics.

### 🛠️ Key Responsibilities & Technical Depth
* **Stream Processing:** Designed the ingestion layer using Kinesis to handle high-velocity e-commerce events with zero data loss.
* **ETL & Transformation:** Developed complex PySpark jobs in AWS Glue for schema enforcement, data partitioning, and columnar storage optimization.
* **Orchestration:** Managed end-to-end workflows using **Apache Airflow (MWAA)**, developing custom DAGs to handle dependency management between Glue jobs and Redshift loads.
* **Data Warehousing:** Loaded curated Gold-layer data into **Amazon Redshift**, optimizing query performance for downstream BI reporting and dashboards.
* **Quality Assurance:** Integrated automated data quality checks at the Bronze-to-Silver transition to ensure downstream data integrity.

### 🚀 Impact
* **Latency Reduction:** Transitioned client from daily batch updates to sub-minute data availability.
* **Performance:** Optimized storage costs and query speeds through efficient partitioning strategies and Parquet conversion.