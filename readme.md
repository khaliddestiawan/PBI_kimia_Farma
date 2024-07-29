# Kimia Farma Analytics

Kimia Farma is one of the oldest and largest pharmaceutical companies in Indonesia. Established in 1817 during the Dutch East Indies era, it started as a small pharmacy in Jakarta. The company was later nationalized in 1958 and became a state-owned enterprise known as Perusahaan Negara Farma.

The dataset in this repository consists of SQL queries and analysis for Kimia Farma.

## Data Model

The Kimia Farma dataset consists of the following three tables:

1. `kf_final_transaction`: Contains the transaction-level data, including customer information, product details, and transaction metadata.
2. `kf_kantor_cabang`: Contains information about the Kimia Farma branch locations, including branch name, city, province, and a branch rating.
3. `kf_product`: Contains details about the products sold by Kimia Farma, including product ID, name, and price.

## SQL Queries

The SQL queries in this repository are designed to transform the raw data into a consolidated table for further analysis.

### `kf_table_analysis.sql`

This query creates a new table called `kf_table_analysis` in the `kimia_farma` dataset. The key steps are:

1. **Common Table Expression (CTE)**: The query uses a CTE to perform the data transformation, which includes:
   - Selecting relevant columns from the source tables
   - Calculating the `rating_cabang`, `gross_laba_percentage`, `nett_sales`, and `rating_transaksi` columns
2. **Final SELECT**: The final `SELECT` statement selects the desired columns from the CTE and calculates the `nett_profit` column by multiplying the `nett_sales` and `gross_laba_percentage` columns.

The purpose of this query is to create a consolidated table that combines transaction data, branch information, and product details, and calculates various metrics such as net sales and net profit. This table can be used for further analysis and reporting on the Kimia Farma business.

## Usage

To run the SQL queries, you will need access to a BigQuery or similar SQL environment. You can copy and paste the queries into your SQL editor and execute them.

Once the `kf_table_analysis` table is created, you can use it for various analytical tasks, such as:

- Generating reports on sales performance, profitability, and customer behavior
- Identifying trends and patterns in the data
- Performing advanced analytics, such as segmentation, forecasting, or predictive modeling

Feel free to explore and build upon the queries provided in this repository to suit your specific analytical needs.