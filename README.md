# 🏏 IPL Data Lakehouse Project

A full end-to-end **Data Lakehouse pipeline** for cricket match analytics using:
- **Azure Data Factory** for orchestration
- **Azure Data Lake Gen2** for storage
- **Azure Databricks** for transformation and machine learning
- **Power BI** for dashboard and reporting

This project processes **IPL cricket datasets** from 2008–2020 and follows the **Medallion Architecture**: Bronze, Silver, and Gold layers.

---

## 🧱 Architecture: Medallion Framework

```mermaid
graph TD
    A[Raw Data (GitHub + Local)] --> B[ADF - Data Ingestion]
    B --> C[ADLS Gen2 - Bronze Layer]
    C --> D[Databricks - Silver Layer]
    D --> E[Databricks - Gold Layer + ML]
    E --> F[Power BI Dashboard]
