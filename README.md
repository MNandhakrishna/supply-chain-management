# Supply Chain Management using Azure Databricks

This project is focused on optimizing supply chain operations by calculating the **shortest delivery routes for customers** and providing insights through interactive dashboards. Built entirely on **Azure** services with **Databricks** at the core, the project follows a robust Medallion Architecture to manage data quality and pipeline stages effectively.

---

## Project Overview

-  **Data Source**: Ingested quarterly (every 3 months) via **Azure Data Factory (ADF)** using event-triggered pipelines.
-  **Storage**: Leveraging **Medallion Architecture** with Bronze, Silver, and Gold layers using Azure Data Lake Storage (ADLS).
-  **Processing**: Data cleaning, transformation, and feature engineering using **Azure Databricks**.
-  **Analysis**: Final dashboards built on top of **Gold Layer** datasets using **Databricks Dashboards**.
-  **Version Control**: Code is maintained and tracked via **GitHub** for collaboration and safety.

---

## Tech Stack

- **Azure Data Factory (ADF)** – Data ingestion and scheduling
- **Azure Databricks** – Data engineering, processing, and dashboarding
- **Azure Data Lake Storage (ADLS)** – Data storage using Medallion Architecture (Bronze, Silver, Gold)
- **GitHub** – Version control and CI/CD (optional)
- **Spark SQL / PySpark** – Data transformations and feature engineering

---

## Data Architecture: Medallion Pattern

1. **Bronze Layer**  
   Raw data ingested from source and saved as external tables.
   
2. **Silver Layer**  
   Cleaned and feature-engineered datasets using Databricks notebooks.
   
3. **Gold Layer**  
   Aggregated and analytical datasets prepared for dashboards and reporting.

---

## Pipeline Flow

1. **Data Ingestion**  
   - Triggered quarterly using ADF
   - Data loaded into the Bronze layer (ADLS)

2. **Processing & Feature Engineering**  
   - External tables created in Databricks
   - Data cleaned, transformed, and saved to Silver

3. **Aggregation & Reporting**  
   - Aggregations performed for business KPIs
   - Saved to Gold layer and visualized through dashboards

---

## Dashboards

- Real-time metrics on delivery route optimization
- Customer-level order fulfillment insights
- Warehouse-to-customer distance visualizations

> Built using Databricks Dashboard features connected to Gold layer datasets.

---

## Scheduling

- **Event-based triggers** used in ADF to automate ingestion.
- Pipelines designed for seamless quarterly updates without manual intervention.

---

## Project Structure 

/notebooks

├── ingestion/

├── cleaning/

├── feature_engineering/

├── aggregation/

└── dashboard/

