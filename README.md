# NYcab-Insights-project

## **Prerequisites**
1. **Google Cloud Platform (GCP):**
   - Ensure you have an active GCP account.
   - Enable the following APIs:
     - Cloud Composer
     - Google Cloud Storage
     - BigQuery
   - Create a Cloud Composer environment and configure it.
   - Create a bucket for raw, processed data, and models (e.g., `nycab-insight-bucket`).

2. **Render Account:**
   - Create an account on Render.com to host the prediction API.

3. **Tools:**
   - Python 3.8+ installed locally or Google Colab for model training.
   - GCP Service Account Key file for authentication.

4. **Environment Configuration:**
   - Install required libraries from `requirements.txt` on your local/virtual environment or in Colab:
     ```bash
     pip install -r requirements.txt
     ```
Step 1: Create Tables in BigQuery
Set Up BigQuery Dataset:

Open the BigQuery Console in GCP.
Create a dataset named nycab_dwh.
Run SQL Scripts to Create Tables:

Use the provided SQL scripts (Table Creation.sql and analytics_tbl.sql) to create required tables for the project.
Navigate to the BigQuery console, select the nycab_dwh dataset, and execute the SQL commands to create the following tables:
Fact Table: fact_trips
Dimension Tables: datetime_dim, location_dim, vendor_dim, Ratecode_dim, payment_type_dim
Analytics Tables: Tables for aggregations and dashboards.
