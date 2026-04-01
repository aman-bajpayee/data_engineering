<h1 align="center">E-commerce Analytics Warehouse using dbt + DuckDB</h1>


## 🧠 Project Overview

This project builds an end-to-end analytics pipeline for an e-commerce business using **dbt and DuckDB**.

It transforms raw transactional data into a **star schema warehouse** with support for:

* Incremental data processing
* Historical tracking using SCD Type-2
* Business-ready aggregated marts

---

## ⚙️ Tech Stack

* Python
* dbt
* DuckDB
* SQL

---

## 🧱 Architecture

```text
Raw Data (CSV)
      ↓
Staging Layer (stg_orders)
      ↓
Snapshot Layer (SCD Type-2)
      ↓
Dimension Tables (dim_customer, dim_product)
      ↓
Fact Table (fact_orders - incremental)
      ↓
Mart Layer (daily_sales, CLV, business_insights)
```

---

## 🔥 Key Features

### 1. Incremental Fact Table

* Processes only new data
* Uses sliding window for late-arriving data

---

### 1. SCD Type-2 Implementation

* Tracks historical changes in customer attributes
* Maintains:

  * `dbt_valid_from`
  * `dbt_valid_to`

---

### 2. Star Schema Design

* Fact table for transactions
* Dimension tables for context

---

### 3. Business Metrics

* Daily revenue trends
* Customer lifetime value
* Revenue by category & city

---

## 📊 Sample Insights

* Revenue distribution across cities
* Top performing product categories
* Customer order behavior

---

## 🚀 How to Run

```bash
dbt seed --full-refresh
dbt run --full-refresh
dbt snapshot
dbt docs generate
dbt docs serve
```

---

## 🧠 Learnings

* Built scalable data pipelines using dbt
* Implemented SCD Type-2 for historical tracking
* Designed star schema for analytics
* Handled schema evolution and debugging

---

## 📌 Future Improvements

* Add Airflow orchestration
* Use real-world dataset
* Deploy on cloud warehouse (BigQuery/Snowflake)

---

# 🧠 4. Resume Bullet Points (Use These)

Add under **Projects**:

```text
• Built an end-to-end analytics warehouse using dbt and DuckDB, implementing a star schema with fact and dimension tables.

• Designed incremental data pipelines with late-arriving data handling, reducing processing overhead.

• Implemented SCD Type-2 snapshots to track historical customer changes using dbt.

• Developed business marts to analyze revenue trends, customer lifetime value, and product performance.

• Debugged real-world issues including schema evolution, data inconsistencies, and environment setup.
```

---

## 📚 Learn & Connect
1. 🔗 **[LinkedIn](https://www.linkedin.com/in/aman-bajpayee-0b8b6016a/)**
