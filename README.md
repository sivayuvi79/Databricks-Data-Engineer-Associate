# Databricks – Data Engineer Associate Practice Repository

This repository contains hands-on exercises, sample data, and Databricks notebooks designed to practice core workflows for the **Databricks Data Engineer Associate certification** while simultaneously implementing a **real end-to-end data engineering project**.

---

## 1. Project Overview

### Objective

Build and practice:

* dimension and fact pipelines
* incremental data processing
* medallion architecture
* SQL and PySpark ETL patterns
* dashboard-ready Gold tables

### Business Case

A large FMCG retail enterprise acquires a smaller company and must:

* consolidate both companies’ datasets
* standardize schemas
* build a unified lakehouse for analytics
* support historical and incremental loads

---

## 2. End-to-End Project: FMCG Retail Merger Data Pipeline

### Project Title

**FMCG Retail Merger Data Pipeline using Databricks Free Edition**

### Summary

This project implements a scalable data engineering pipeline using:

* Databricks Free Edition
* PySpark and SQL
* Medallion Lakehouse Architecture

The pipeline ingests raw retail data from both companies, cleans and conforms datasets, and publishes analytical Gold tables consumed by BI dashboards.

### Core Deliverables

* Raw → Bronze → Silver → Gold pipeline
* Historical and incremental data ingestion
* Data quality and validation checks
* Automated workflow execution
* Dashboard-ready analytical tables

### Technology Stack

* Databricks Free Edition
* PySpark and Spark SQL
* Amazon S3 / DBFS storage
* Power BI / Tableau for visualization (optional)

---

## 3. Architecture Overview

### Components

1. **Data Sources**

   * sales, inventory, products, customers, stores

2. **Landing Zone (Raw)**

   * S3/DBFS raw CSV files

3. **Bronze Layer**

   * schema enforcement
   * ingestion logs

4. **Silver Layer**

   * cleansing
   * deduplication
   * conformed dimensions

5. **Gold Layer**

   * star schema
   * aggregated fact tables

6. **BI Layer**

   * KPI dashboards and reporting

### Data Flow

S3/DBFS Raw → Bronze → Silver → Gold → BI

---

## 4. Data Modeling

Dimension tables:

* dim_product
* dim_customer
* dim_store

Fact tables:

* fact_sales
* fact_inventory

Historical tracking uses effective-date style versioning where applicable.

---

## 5. Implementation Steps (High Level)

1. Create Databricks environment
2. Upload or mount dataset
3. Build Bronze ingestion tables
4. Clean and transform to Silver
5. Model Gold layer for analytics
6. Implement incremental ingestion
7. Run data validation checks
8. Build dashboard queries

---

## 6. Repository Structure

```
project-fmcg/
│
├── codes/
│   ├── 1_setup/
│   ├── 2_dimension_data_processing/
│   └── 3_fact_data_processing/
│
├── dashboarding/
├── data/
└── resources/
```

### Key folders

* **1_setup**

  * catalog setup
  * utilities
  * date dimension creation

* **2_dimension_data_processing**

  * customers
  * products
  * pricing

* **3_fact_data_processing**

  * full loads
  * incremental loads

---

## 7. Notebooks Execution Order

1. setup
2. dimensions
3. facts

---

## 8. Requirements

* Databricks workspace (recommended)
* or local Spark environment
* Python 3.8+

Optional libraries when running locally:

```
pip install pandas pyspark notebook
```

---

## 9. Quick Start – Databricks

1. Import notebooks from `project-fmcg/codes/`
2. Upload or mount `data/`
3. Execute notebooks in required sequence:

* setup
* dimensions
* facts

---

## 10. License

This repository is intended for **learning and certification practice**.

---
