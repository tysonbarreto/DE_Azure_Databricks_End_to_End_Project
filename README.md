
# ⚙️ Azure Data Engineering Pipeline

A modular, production-grade data engineering solution combining **Azure Data Factory** for ETL and **Azure Databricks** for real-time streaming and analytics. This project demonstrates scalable, fault-tolerant data movement and transformation using modern cloud-native tools.

---

## 📌 Project Overview

This pipeline consists of two integrated components:

### 1️⃣ Azure Data Factory – Incremental ETL with CDC
- Implements **Change Data Capture (CDC)** for multiple source tables  
- Performs **conditional update checks** and **incremental loads**  
- Integrates **Logic Apps** for failure notifications and alerting  
- Ensures data freshness and operational transparency

### 2️⃣ Azure Databricks – Streaming & Lakehouse Processing
- Streams ingested data from **ADLS Gen2** using **Delta Lake**  
- Utilizes **LakeFlow** and **AutoLoader** for declarative ingestion  
- Applies **checkpointing** and **idempotency** for reliable processing  
- Uses **Jinja templating** for dynamic pipeline configuration  
- Computes real-time metrics and supports downstream analytics

---

## 🗂️ Folder Structure

```
project-root/
├── adf/
│   └── cdc_pipeline.json         # ADF pipeline definition with CDC logic
│   └── logic_app_alerts.json     # Logic App for failure notifications
├── databricks/
│   └── lakeflow_ingestion.py     # Declarative streaming with AutoLoader
│   └── jinja_templates/          # Configurable templates for pipeline logic
│   └── checkpoint_config.json    # Checkpointing and idempotency setup
```

---

## 🚀 Key Features

- ✅ Incremental ETL with CDC  
- 🔁 Stream ingestion with AutoLoader  
- 🧩 Config-driven pipelines via Jinja  
- 🛡️ Idempotent and fault-tolerant design  
- 📣 Alerting via Logic Apps  
- 📊 Delta Lake for scalable analytics

---

## 🧪 Prerequisites

- Azure Data Factory with access to source systems  
- Azure Logic Apps for alerting  
- Azure Databricks workspace with Unity Catalog  
- ADLS Gen2 configured for Delta Lake storage  
- Python 3.8+ and required Databricks libraries

---

## 📈 Next Steps

- Extend CDC logic to additional domains  
- Integrate with Power BI or Azure Synapse for reporting  
- Add data quality checks and lineage tracking  
- Enable schema evolution and audit logging
