Microsoft Fabric Medallion Architecture

An end-to-end data engineering project built with Microsoft Fabric, Lakehouse, Notebooks, and Data Pipeline Orchestration.

!Microsoft Fabric !Architecture !GitHub

📌 Project Overview

This project demonstrates the implementation of an end-to-end data engineering workflow using Microsoft Fabric and the Medallion Architecture.

The solution organizes data processing into multiple layers, from raw data ingestion to curated, analytics-ready datasets. Fabric notebooks handle the transformation stages, while a central pipeline orchestrates the workflow.

The project is designed to demonstrate practical skills in data ingestion, data transformation, Lakehouse architecture, and workflow orchestration.

🏗️ Architecture

<!-- Add your architecture diagram to the architecture/ folder and update this path if needed. -->

!Fabric Project Architecture

Data Flow
mermaid
flowchart LR
    A[Source Systems] --> B[Landing Layer]
    B --> C[Bronze Layer]
    C --> D[Silver Layer]
    D --> E[Gold Layer]
    E --> F[Analytics and Reporting]

    style B fill:#dbeafe,stroke:#2563eb,color:#111827
    style C fill:#fce7d6,stroke:#c2410c,color:#111827
    style D fill:#e5e7eb,stroke:#6b7280,color:#111827
    style E fill:#fef08a,stroke:#ca8a04,color:#111827

🥉 Medallion Layers
Layer	Purpose
Landing	Receives raw data from source systems.
Bronze	Stores ingested data for downstream processing.
Silver	Applies data cleaning, standardization, and transformation.
Gold	Contains curated datasets prepared for analytical use.

Each layer has a distinct responsibility, helping organize the processing workflow and maintain a clear separation between raw, transformed, and analytical data.

⚙️ Technologies Used
Microsoft Fabric — Unified data engineering and analytics platform.
Fabric Lakehouse — Lakehouse storage for the data layers.
Fabric Notebooks — Data ingestion and transformation logic.
Fabric Data Pipelines — Workflow orchestration and activity dependencies.
SQL Analytics Endpoints — SQL-based access to Lakehouse data.
Git and GitHub — Source control and project documentation.
🔄 Pipeline Orchestration

The project includes an End to End Orchestration pipeline that coordinates the main processing stages.

mermaid
flowchart TD
    A[Raw to Landing] -->|Success| B[Landing to Bronze]
    B -->|Success| C[Silver Transformations]
    C -->|Success| D[Gold Layer]

    style A fill:#dbeafe,stroke:#2563eb,color:#111827
    style B fill:#fed7aa,stroke:#c2410c,color:#111827
    style C fill:#e5e7eb,stroke:#6b7280,color:#111827
    style D fill:#fef08a,stroke:#ca8a04,color:#111827

Pipeline Activities
Activity	Type	Responsibility
Raw to Landing	Invoke Pipeline	Starts the data ingestion workflow.
Landing to Bronze	Notebook	Processes
