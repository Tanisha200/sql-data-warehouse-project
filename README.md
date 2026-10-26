# sql-data-warehouse-project
# SQL Data Warehouse Project

## About the Project

This project builds a modern data warehouse in SQL Server using data from two source systems: CRM and ERP.

Raw CSV files are loaded, cleaned, transformed, and modeled into business-ready tables for reporting and analysis. The final data is organized in a star schema and supports analysis of customer behavior, product performance, and sales trends.

## Data Architecture

The project follows the Medallion Architecture with three layers:

| Layer | Purpose |
|---|---|
| Bronze | Stores raw data exactly as received from the CRM and ERP CSV files |
| Silver | Cleans, standardizes, and prepares the data for analysis |
| Gold | Contains business-ready data modeled into fact and dimension tables for reporting |

## Project Overview

In this project, I:

- Designed a three-layer data warehouse architecture: Bronze, Silver, and Gold
- Built ETL pipelines to load CSV source files into SQL Server
- Cleaned and standardized data quality issues
- Integrated CRM and ERP data into a single analytical data model
- Modeled facts and dimensions for reporting
- Wrote SQL queries to analyze customer behavior, product performance, and sales trends

## Repository Structure

```text
sql-data-warehouse-project/
├── 00_setup/
│   └── Setup guide and Docker startup files
├── 01_datasets/
│   ├── source_crm/
│   │   └── CRM source files
│   └── source_erp/
│       └── ERP source files
├── 02_docs/
│   └── Requirements, diagrams, and project notes
├── 03_scripts/
│   ├── init_database.sql
│   ├── bronze/
│   │   └── Loads raw source data
│   ├── silver/
│   │   └── Cleans and prepares data
│   └── gold/
│       └── Builds analytical tables
└── 04_tests/
    └── Data quality checks
```

## Getting Started

1. Install SQL Server and SQL Server Management Studio (SSMS).
2. Open the setup guide in the `00_setup` folder.
3. Create the database by running:

```sql
03_scripts/init_database.sql
```

4. Load the raw data using the scripts in:

```text
03_scripts/bronze/
```

5. Clean and transform the data using:

```text
03_scripts/silver/
```

6. Build the final analytical tables using:

```text
03_scripts/gold/
```

## Data Source Path

The project expects the six source CSV files to be available at:

```text
C:\sql\dwh_project\01_datasets\
```

If the files are stored in a different location, update the file paths in:

```text
03_scripts/bronze/proc_load_bronze.sql
```

## Technologies Used

- SQL Server
- SQL Server Management Studio
- SQL
- CSV data sources
- Medallion Architecture
- Star Schema data modeling

## Analytics Covered

The Gold layer supports SQL-based analysis of:

- Customer behavior
- Product performance
- Sales trends

## Author

**Tanisha Singh**  
Data Engineer | SQL Server & Data Analytics
