# Azure End-to-End Data Engineering AdventWork Project
This repository contains a data engineering pipeline developed around a made-up business use case. 
It was created as a hands-on learning exercise to strengthen my skills in building and managing end-to-end data pipelines.

## Project Overview
This project tackles a key business requirement by implementing a full-scale data pipeline using Azure services. It focuses on extracting customer and sales data from an on-premises SQL database, transforming it in the cloud, and delivering actionable insights via a Power BI dashboard. The dashboard showcases critical KPIs such as gender distribution and product category sales, with interactive filters for date, product category, and gender to support informed decision-making.

## Business Request
The company has identified a need to better understand customer demographics—particularly the gender distribution—and how it impacts purchasing behavior. A large volume of customer data currently resides in an on-premises SQL database. Stakeholders have requested the development of a KPI dashboard that delivers clear insights into sales performance segmented by gender and product category. The dashboard should display key metrics such as total products sold, total revenue, and a visual breakdown of customer gender. It must also include intuitive filtering options by product category, gender, and support date-based queries through a user-friendly interface.

## Solution Overwiew
To fulfill the project requirements, the solution is structured into the following key components:

1. Data Ingestion
    - Extract customer and sales data from an on-premises SQL database.
    - Ingest the data into Azure Data Lake Storage (ADLS) using Azure Data Factory (ADF).

2. Data Transformation
    - Process and transform the ingested data using Azure Databricks.
    - Implement a Medallion Architecture by structuring the data into Bronze (raw), Silver (cleansed), and Gold (aggregated) layers.

3. Data Loading & Visualization
    - Load the refined data into Azure Synapse Analytics for advanced querying and analysis.
    - Develop a Power BI dashboard to visualize key metrics, enabling stakeholders to interact with sales and demographic data through filters by date, gender, and product category.

4. Automation
    - Automate the entire pipeline to run on a daily schedule, ensuring consistent and up-to-date reporting.

5. CI/CD Integration
    - Implement CI/CD pipelines using Azure DevOps Actions to automate deployment and version control of data pipeline components (e.g., ADF pipelines, Synapse scripts, and Databricks notebooks).

## Technology Stack
  - Azure Data Factory (ADF) – Orchestrates data movement and transformation workflows.
  - Azure Data Lake Storage (ADLS) – Serves as the central repository for both raw and processed data.
  - Azure Databricks – Handles data transformation, cleansing, and advanced processing.
  - Azure Synapse Analytics – Provides data warehousing and supports powerful SQL-based analytics.
  - Power BI – Delivers interactive data visualizations and business reporting.
  - Azure Key Vault – Secures sensitive information such as secrets, credentials, and connection strings.
  - SQL Server (On-Premises) – Acts as the primary data source for customer and sales information.
  - Azure DevOps – Facilitates Continuous Integration and Continuous Deployment (CI/CD) for pipeline automation and version control.
