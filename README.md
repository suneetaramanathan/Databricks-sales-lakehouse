Sales Lakehouse on Databricks (Medallion Architecture)

End-to-end data pipeline on **Databricks** using **PySpark** and **Delta Lake**, following the
Bronze → Silver → Gold medallion architecture on the TPC-H sales dataset (7.5M orders, 750K customers).

## Architecture
| Layer | Tables | What happens |
|---|---|---|
| **Bronze** | `bronze_orders`, `bronze_customer`, `bronze_nation`, `bronze_region` | Raw ingestion + metadata (`_ingested_at`, `_source`) |
| **Silver** | `silver_orders`, `silver_customers`, `quarantine_orders` | Renaming, type casting, deduplication, 5 data-quality rules, invalid rows quarantined, customers enriched with country & region |
| **Gold** | `gold_revenue_by_region_month`, `gold_segment_performance`, `gold_top_customers` | Business KPIs: revenue, orders, AOV, customer lifetime value |

## Features
- **Unity Catalog** schema with documented tables (table comments)
- **Data quality checks** with a quarantine table instead of silent data loss
- **Delta Lake**: version history (`DESCRIBE HISTORY`), time travel, `OPTIMIZE`
- **Databricks Job** scheduled daily on serverless compute

## Results
- 7,500,000 orders processed; 0 failed data-quality rules; 750,000 enriched customers
- Daily scheduled job: successful run in 2 min 23 s
- Note: TPC-H is synthetic, uniformly generated benchmark data, so KPIs are evenly distributed across regions and segments.

## Tech
Databricks · PySpark · Delta Lake · Unity Catalog · SQL · Databricks Jobs

## Scheduled job run
![Databricks job run](job_run.png)# Sales Lakehouse on Databricks (Medallion Architecture)

End-to-end data pipeline on **Databricks** using **PySpark** and **Delta Lake**, following the
Bronze → Silver → Gold medallion architecture on the TPC-H sales dataset (7.5M orders, 750K customers).

## Architecture
| Layer | Tables | What happens |
|---|---|---|
| **Bronze** | `bronze_orders`, `bronze_customer`, `bronze_nation`, `bronze_region` | Raw ingestion + metadata (`_ingested_at`, `_source`) |
| **Silver** | `silver_orders`, `silver_customers`, `quarantine_orders` | Renaming, type casting, deduplication, 5 data-quality rules, invalid rows quarantined, customers enriched with country & region |
| **Gold** | `gold_revenue_by_region_month`, `gold_segment_performance`, `gold_top_customers` | Business KPIs: revenue, orders, AOV, customer lifetime value |

## Features
- **Unity Catalog** schema with documented tables (table comments)
- **Data quality checks** with a quarantine table instead of silent data loss
- **Delta Lake**: version history (`DESCRIBE HISTORY`), time travel, `OPTIMIZE`
- **Databricks Job** scheduled daily on serverless compute

## Results
- 7,500,000 orders processed; 0 failed data-quality rules; 750,000 enriched customers
- Daily scheduled job: successful run in 2 min 23 s
- Note: TPC-H is synthetic, uniformly generated benchmark data, so KPIs are evenly distributed across regions and segments.

## Tech
Databricks · PySpark · Delta Lake · Unity Catalog · SQL · Databricks Jobs

## Scheduled job run
![Databricks job run](job_run.png)# Sales Lakehouse on Databricks (Medallion Architecture)

End-to-end data pipeline on **Databricks** using **PySpark** and **Delta Lake**, following the
Bronze → Silver → Gold medallion architecture on the TPC-H sales dataset (7.5M orders, 750K customers).

## Architecture
| Layer | Tables | What happens |
|---|---|---|
| **Bronze** | `bronze_orders`, `bronze_customer`, `bronze_nation`, `bronze_region` | Raw ingestion + metadata (`_ingested_at`, `_source`) |
| **Silver** | `silver_orders`, `silver_customers`, `quarantine_orders` | Renaming, type casting, deduplication, 5 data-quality rules, invalid rows quarantined, customers enriched with country & region |
| **Gold** | `gold_revenue_by_region_month`, `gold_segment_performance`, `gold_top_customers` | Business KPIs: revenue, orders, AOV, customer lifetime value |

## Features
- **Unity Catalog** schema with documented tables (table comments)
- **Data quality checks** with a quarantine table instead of silent data loss
- **Delta Lake**: version history (`DESCRIBE HISTORY`), time travel, `OPTIMIZE`
- **Databricks Job** scheduled daily on serverless compute

## Results
- 7,500,000 orders processed; 0 failed data-quality rules; 750,000 enriched customers
- Daily scheduled job: successful run in 2 min 23 s
- Note: TPC-H is synthetic, uniformly generated benchmark data, so KPIs are evenly distributed across regions and segments.

## Tech
Databricks · PySpark · Delta Lake · Unity Catalog · SQL · Databricks Jobs

## Scheduled job run
![Databricks job run](job_run.png)
