# AWS + Power BI Serverless Analytics Pipeline

This project demonstrates how to build a **serverless, cloud-based data analytics pipeline** using **Amazon Web Services (AWS)** and **Power BI**. 
It was designed to showcase beginner-friendly, real-world cloud skills for data analysis, reporting, and business intelligence.

---

##  Project Overview

- **Data Source**: Cleaned Financial data in CSV format
- **Cloud Storage**: Amazon S3
- **Query Engine**: AWS Athena (serverless SQL querying on S3)
- **Optional Schema Discovery**: AWS Glue Crawler
- **Data Visualization**: Microsoft Power BI (connected via ODBC)

---

##  Tools & Services Used

| Tool/Service | Purpose |
|--------------|---------|
| **Amazon S3** | Store raw and cleaned CSV data |
| **AWS Athena** | Query data directly from S3 using SQL |
| **AWS Glue** | Automatically detect schema from data |
| **Power BI** | Connects to Athena via ODBC to visualize results |
| **ODBC Driver** | Enables Power BI to connect to Athena |
| **AWS IAM** | Manage permissions securely |

---

##  Architecture Diagram

```
┌────────────┐     ┌──────────────┐     ┌────────────────┐     ┌────────────┐     ┌───────────────┐     ┌────────────┐     ┌────────────┐
│  Amazon S3 │ ──▶ | AWS Glue    │ ──▶ │ Glue Data      │ ──▶│ AWS Athena │ ──▶ │ SQL Query     │ ──▶│ ODBC Driver │ ──▶|  Power BI  │
│ (CSV files)│     │ Crawler      │     │ Catalog (Table │     │(QueryEngine)|     │(SELECT ...)  │     │ (Athena Conn)│    │ Dashboard │
└────────────┘     └──────────────┘     └────────────────┘     └────────────┘     └───────────────┘     └────────────┘     └────────────┘
                                                                                                                                  
                                                                                                                              
┌──────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│                                              IAM Roles & Permissions                                                       │
│ - Glue Crawler: Read access to Amazon S3                                                                                      │
│ - Glue & Athena: Access to Glue Data Catalog                                                                                  │
│ - Athena: Read/query permissions on S3 bucket                                                                                 │
│ - ODBC/Power BI: IAM User with programmatic access (Access Key + Secret) for Athena connection                               │
└──────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┘
```
 How It Works

Upload Dataset: Financial data (CSV) is uploaded to an S3 bucket.

Define Schema: Athena table is manually created (or auto-detected with Glue).

Run SQL Queries: Athena reads the data without moving it.

Connect Power BI: Using ODBC driver, Power BI fetches data for visual dashboards.

 Sample Visuals
See screenshots folder for Power BI dashboards, S3 structure, and Athena output.

 Author
---
Sri Naga

Cloud Enthusiast | AWS & Power BI 
📍 Open to Cloud based roles, Data Analyst, or BI Analyst roles

🔗 LinkedIn Profile https://www.linkedin.com/in/sri-naga-p

This project uses public Financial data (e.g., from Kaggle)

Designed as a beginner-friendly cloud BI project

Can be extended with AWS Lambda, QuickSight, or Glue jobs

 What I Learned

Hands-on experience with AWS S3, Athena, Glue, and IAM

Building data pipelines without servers

Querying cloud-based data and building dashboards with Power BI

Connecting AWS to BI tools securely and effectively

📢 Hire Me!
If you're looking for a motivated cloud & data learner who loves solving real-world problems — I'm ready! 🚀

“This project was developed to demonstrate my skills in building real-world cloud-based analytics pipelines using AWS and Power BI.”

#aws #powerbi #serverless #datapipeline #cloudproject



