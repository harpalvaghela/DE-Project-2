# Project 2: Transactions and Loan Data Pipeline (Azure + Databricks)

## 📌 Objective

This project builds a robust and scalable data pipeline using **Azure Data Lake Storage Gen2**, **Databricks Notebooks**, and **Delta Lake** to process, transform, and analyze **customer account, loan, payment, and transaction data**.

The pipeline supports daily ingestion, transformation, Slowly Changing Dimensions (SCD Type 1), and integration with **Power BI** for business reporting.


**🛠Technologies Used:**

- Azure Data Lake Gen2 (ADLS)
- Azure Key Vault (for secure SAS/key storage)
- Databricks (PySpark & SQL)
- Delta Lake for ACID-compliant data operations
- Power BI for reporting and visualization
- Azure Databricks Workflows for scheduling

**Folder Structure in ADLS Gen 2:**

/project2/
│
├── bronze/                    # Raw source files in date-partitioned folders
├── silver/                    # Cleaned & transformed data (Parquet / Delta)
├── gold/                      # Final SCD Type 1 output for reporting
├── client_backup_files/      # Backup of daily CSVs in year/month/day format


**Pipeline Steps**
Step 1: Bronze Layer (Raw Ingestion)
CSV files for accounts, customers, loans, payments, transactions

Stored as /bronze/YYYY/MM/DD/*.csv

Step 2: Silver Layer (Data Cleaning & Transformations)
Null checks, deduplication, type casting

Written in Parquet/Delta format

Step 3: Gold Layer (SCD Type 1)
Merge logic using Delta's MERGE INTO

Final Delta tables registered for Power BI

Step 4: Power BI Integration
Databricks SQL endpoint connects to Delta tables

Visualizations: Top Accounts, Loan Trends, Transaction Volume

**Notable Features**
📂 Fully date-partitioned ingestion

🧼 Modular transformation functions

🧠 SCD Type 1 Delta merge logic

♻️ Backup of raw CSVs with rename logic

📊 Live connection to Power BI via SQL Warehouses

📅 Workflow-ready via Databricks Jobs


---------------------------------------------------------

Connect with me on my profile below for more updates:

LinkedIn: https://www.linkedin.com/in/harpalvaghela/

Medium Blog: https://medium.com/@harpalvaghela

Thank you
