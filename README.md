**Azure Databricks Retail Lakehouse Project**

This project implements an end-to-end Data Engineering pipeline using Azure Databricks and Azure Data Lake Storage (ADLS) on a retail dataset containing Orders, Customers, and Products.

Raw Parquet files are ingested from ADLS into Bronze, cleaned and standardized in Silver, and transformed into analytics-ready tables in the Gold layer following the Lakehouse architecture.

**In the Gold layer:**

Customers are modeled using SCD Type 1 to keep the latest customer data (dim_customers)

Products are modeled using SCD Type 2 using Delta Live Tables (DLT) to track full change history (dim_products)

Orders are joined with customer and product dimensions to create a fact table (fact_orders)

The project uses Unity Catalog, storage credentials, and external locations to securely access Azure Data Lake from Databricks.

This solution demonstrates real-world cloud data engineering, dimensional modeling, and slowly changing dimensions in an Azure Lakehouse environment.
