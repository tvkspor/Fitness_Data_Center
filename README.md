# Fitness_Data_Center

##  Overview

This project demonstrates a complete data ingestion pipeline for fitness tracking data using real-time and batch data processing technologies. The pipeline integrates user registration, profile updates, heart rate (BPM) streaming, and workout session data from fitness devices and mobile applications into a unified analytics platform.

---

##  Key Features

- **Data Ingestion**:
  - Integrated user registration and login/logout events via **Azure SQL**.
  - Streamed **BPM and workout session** data using **Apache Kafka** via Kafka Connect.
  
- **ETL Workflows**:
  - Designed and implemented **incremental ETL workflows** to handle CDC (Change Data Capture) for user profiles and real-time heart rate data.
  - Processed workout session data to extract **user activity summaries** and performance metrics.

- **Data Governance**:
  - Utilized **Unity Catalog** in Databricks for managing data access, lineage, and security across bronze, silver, and gold data layers.

- **Storage Architecture**:
  - Architected a **multi-layered storage strategy** using **Azure Data Lake Storage Gen2 (ADLS Gen2)** with Bronze (raw), Silver (cleansed), and Gold (aggregated) zones.

- **Data Processing & Analytics**:
  - Deployed **Spark applications** in Databricks clusters to handle:
    - Real-time stream ingestion.
    - Batch transformations and aggregation.
  - Created **interactive dashboards** to visualize fitness metrics such as:
    - BPM trends.
    - Workout completion rates.
    - Gym activity summaries.

- **Automation & Monitoring**:
  - Ensured robust **pipeline scheduling**, **error handling**, and **monitoring mechanisms** to enable end-to-end automated data processing.

---

## Sample Data Flow

1. **Registration/Login** → Azure SQL → Bronze → Silver → Gold → Dashboards
2. **User Profile Updates (CDC)** → Kafka → Bronze → Silver
3. **BPM Streaming Data** → Kafka → Multiplex Table → Bronze → Silver → Gold
4. **Workout Sessions** → Kafka → Bronze → Silver → Gold

---

## Technologies Used

- **Cloud Platform**: Microsoft Azure
  - Azure Data Lake Storage (ADLS) Gen2
  - Azure SQL Database
- **Big Data & Processing**:
  - Databricks (Spark, Unity Catalog)
- **Streaming**:
  - Apache Kafka (via Kafka Connect)

---

## Outcomes

- Real-time BPM stream monitoring.
- Historical user fitness behavior analysis.
- Scalable and secure cloud data architecture ready for production.

---

## Architecture Diagrams

<img src="Picture/Architecture Image.png" alt="Databricks Lakehouse Pipeline" width="600"/>


