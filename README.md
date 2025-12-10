📦 Retail Azure Data Engineering Project

🚀 End-to-End Azure Data Pipeline for a Retail Client
This project demonstrates a complete Azure Data Engineering solution for a retail client, covering ingestion, processing, transformation, storage, and reporting using modern Azure services.
The goal is to build a pipeline that handles multiple data sources, processes them into clean and analytical formats, and produces business-ready insights through Power BI.

🚀 Business Requirements
•	Build a complete data pipeline for a retail client.
•	Ingest data from multiple sources into a Data Lake.
•	Azure SQL DB: Transactions, Products, Stores data.
•	API (JSON): Customer data.
•	Clean, transform, join, and aggregate data for analytics.
•	Deliver insights using Power BI dashboards.
🏗️ Architecture Overview
🔹 Services Used
•	Azure Data Factory (ADF) – Ingestion & orchestration
•	Azure Data Lake Storage Gen2 (ADLS) – Bronze, Silver, Gold layers
•	Azure Databricks – Data cleaning, transformation & Delta Lake
•	Azure SQL Database – Transaction, Store & Product tables
•	Power BI – Visualization and reporting
📌 Layers in ADLS
•	Bronze Layer: Raw ingestion (JSON, SQL tables)
•	Silver Layer: Cleaned, transformed, and joined data
•	Gold Layer: Aggregated, business-ready datasets
📸 Architecture Diagram:
(placed inside screenshots/architecture.png)
🏗️  Data Flow Summary
1. Ingestion (ADF)
•	Copy SQL DB tables → Bronze layer
•	Fetch Customer JSON API → Bronze layer
•	Organized into: customer/, product/, store/, transaction/
2. Processing (Databricks)
•	Read Bronze data
•	Clean, cast, remove duplicates
•	Create Silver curated data
•	Join datasets to build unified tables
•	Create Gold aggregated outputs
o	Sales summary
o	Product performance
o	Store-level insights
📸 Power BI Dashboard
Gold layer data (exported as CSV for free Databricks environment) is used to build:
•	Total Sales Overview
•	Sales by Product
•	Sales by Store
•	Customer Segmentation
•	Transaction Trends
📸 Screenshot:
screenshots/powerbi_dashboard.png

📸 Repository Structure

Retail-Azure-Project/
│
├── data/
│     ├── customer.json
│     ├── product.json
│
├── adf/
│     ├── factory/
│     ├── linkedTemplates/
│     ├── ARMTemplateForFactory.json
│     ├── ARMTemplateParametersForFactory.json
│
├── databricks/
│     ├── retail_project_notebook.ipynb
│  
├── sql/
│     ├── script.sql
│
├── powerbi/
│     ├── Retail_Dashboard.pbix
│
├── screenshots/
│     ├── architecture.png
│     ├── pipeline_overview.png
│     ├── powerbi_dashboard.png
│
└── README.md



📸 Skills Highlighted
•	ETL using ADF
•	Medallion Architecture (Bronze→Silver→Gold)
•	Databricks + PySpark transformations
•	Delta Lake
•	SQL Data Modeling
•	Power BI Reporting
•	GitHub Project Structuring




