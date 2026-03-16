Overview:

This project simulates a real-world vehicle fleet reliability data platform designed to analyze large volumes of vehicle service, telemetry, and repair records. The goal of the project is to demonstrate how data engineering pipelines can support engineering teams in monitoring vehicle reliability and improving product quality.

The platform processes large datasets representing vehicle fleets, service repairs, and component failures. It builds automated ETL pipelines, calculates reliability KPIs, performs anomaly detection, and presents insights through interactive dashboards.

This project reflects how modern data engineering systems can help organizations manage large operational datasets and support data-driven decision making.
______________________________________________________________________________________________________________________________________________________________________

Problem Statement:

Modern vehicle fleets generate large amounts of service and operational data. Engineers must analyze this data to identify patterns such as:

1) frequently failing components

2) vehicles with abnormal repair rates

3) regions with higher service demand

4) trends in vehicle reliability over time

However, raw service and telemetry data is often messy, distributed, and difficult to analyze. This project demonstrates how data pipelines and analytics tools can organize this information and turn it into actionable insights.
______________________________________________________________________________________________________________________________________________________________________

Project Architecture:

Raw Data → ETL Pipeline → Processed Tables → KPI Layer → Dashboard → Anomaly Detection

The system performs the following steps:

1) Generate or ingest vehicle fleet datasets

2) Clean and standardize raw service and telemetry data

3) Transform datasets using SQL and Python

4) Store processed data in a structured format

5) Compute reliability metrics and KPIs

6) Detect unusual patterns using anomaly detection models

7) Present insights through an interactive dashboard
_____________________________________________________________________________________________________________________________________________________________________________

Key Features:

1) ETL Data Pipeline: Automated data ingestion and transformation using Python and SQL ; Data cleaning, schema standardization, and dataset integration ; Scalable pipeline design for processing large datasets

2) Reliability KPI Analytics: Repair rate by vehicle model ; Mean time between failures ; Average repair cost and downtime ; Repeat repair frequency ; Top failing components ; Regional reliability performance

3) Anomaly Detection: An Isolation Forest model is used to detect abnormal vehicle behavior such as unusually high repair frequency, abnormal warranty costs, excessive warning counts from telemetry data. This allows engineers to proactively identify potential reliability issues.

4) Interactive Dashboard: An interactive Streamlit dashboard provides fleet reliability overview, service trends over time, component failure analysis, regional performance comparison, anomaly alerts
_____________________________________________________________________________________________________________________________________________________________________________

Project Structure:

fleet-reliability-platform/

data/
    raw/
    processed/
    synthetic/

notebooks/
    01_data_generation.ipynb
    02_data_cleaning.ipynb
    03_feature_engineering.ipynb
    04_kpi_analysis.ipynb
    05_anomaly_detection.ipynb

sql/
    create_tables.sql
    transform_queries.sql
    kpi_queries.sql

src/
    data_generator.py
    etl_pipeline.py
    feature_engineering.py
    anomaly_detection.py
    utils.py

app/
    streamlit_app.py

outputs/
    charts/
    reports/

requirements.txt
README.md
