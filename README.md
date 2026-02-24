# Enterprise-Grade Databricks Lakehouse Implementation

## Overview

This repository demonstrates a production-style **Data Lakehouse architecture** implemented on Databricks using the Medallion (Bronze–Silver–Gold) framework.

The project simulates CRM and ERP source systems integrated into a unified analytical model to support Sales and Customer Analytics use cases.

It covers the full lifecycle:

- Data ingestion
- Data transformation & cleansing
- Dimensional modeling
- Pipeline orchestration
- Performance optimization

---

## Project Objective

This project demonstrates the design and implementation of a complete **Data Lakehouse architecture** using Databricks and the Medallion (Bronze–Silver–Gold) framework.

The objective is to simulate how modern data platforms are built in enterprise environments — starting from raw source data and progressively transforming it into clean, validated, analytics-ready datasets.

The implementation includes:

- End-to-end ingestion of CRM and ERP datasets
- Structured Medallion architecture design
- Data quality enforcement and validation
- Dimensional modeling using a star schema
- Notebook orchestration and automation
- Delta Lake optimization techniques

This implementation reflects best practices used in enterprise data engineering teams for building scalable and maintainable Lakehouse platforms.

---

## Business Scenario

Organizations often operate multiple systems (CRM, ERP, operational databases).  
This project demonstrates how raw operational data can be consolidated and transformed into analytics-ready fact and dimension tables using modern Lakehouse architecture.

The final Gold layer supports:

- Sales performance analysis
- Customer segmentation
- Product analytics
- Business KPI reporting
- Executive dashboard consumption

---

## Architecture

This project follows the **Medallion Architecture** pattern.

### 🥉 Bronze Layer – Raw Ingestion

- Ingest raw CRM and ERP datasets
- Store data in Delta format
- Maintain schema consistency
- Support incremental ingestion
- Preserve source-level granularity

### 🥈 Silver Layer – Data Standardization

- Data cleansing and validation
- Type casting and schema enforcement
- Deduplication and business rule application
- Creation of standardized, conformed datasets

### 🥇 Gold Layer – Business Transformation

- Star schema dimensional modeling
- Creation of fact and dimension tables
- Aggregated KPI-ready datasets
- Optimized tables for BI and analytics consumption

---

## Project Structure

```
03-DATABRICKS-BIKE-SALES-LAKEHOUSE/
│
├── docs/ # Documentation and supporting material
│
├── datasets/ # Raw source datasets
│ ├── source_crm/
│ │ ├── cust_info.csv
│ │ ├── prd_info.csv
│ │ └── sales_details.csv
│ │
│ └── source_erp/
│ ├── CUST_AZ12.csv
│ ├── LOC_A101.csv
│ └── PX_CAT_G1V2.csv
│
├── script/ # Databricks notebooks (Bronze/Silver/Gold)
│ ├── bronze/
│ │ ├── bronze_crm_ingestion.ipynb
│ │ ├── bronze_erp_ingestion.ipynb
│ │
│ ├── silver/
│ │ ├── silver_crm_customers.ipynb
│ │ ├── silver_erp_products.ipynb
│ │ ├── silver_orchestration.ipynb
│ │
│ ├── gold/
│ │ ├── gold_dim_customers.ipynb
│ │ ├── gold_dim_products.ipynb
│ │ ├── gold_fact_sales.ipynb
│ │ ├── gold_orchestration.ipynb
│ │
│ └── init_lakehouse.ipynb
│
├── .gitignore
├── LICENSE
└── README.md

```

---

## Technologies Used

- Databricks
- Apache Spark
- PySpark
- Spark SQL
- Delta Lake
- Unity Catalog

---

## Key Concepts Demonstrated

- Medallion Architecture
- Delta Lake table management
- Incremental data processing
- Data quality enforcement
- Dimensional modeling (Star Schema)
- Notebook orchestration
- Lakehouse optimization techniques (partitioning, optimization)

---

## How to Run

1. Initialize environment using `init_lakehouse.ipynb`
2. Execute Bronze layer notebooks
3. Run Silver transformations
4. Execute Gold layer notebooks
5. Validate final fact and dimension outputs

---

## Acknowledgment

This project draws conceptual inspiration from the Databricks Lakehouse Bootcamp by **Baraa Khatib Salkini**.

The architecture, notebook structure, and enhancements in this repository were independently implemented and adapted to simulate enterprise-level data engineering practices.

---

## Author

Mohammed Afzal Shariff  
BI Associate Manager | Data & Analytics Professional  
Bengaluru, India
