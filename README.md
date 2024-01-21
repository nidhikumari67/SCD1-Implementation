# SCD1-Implementation

## Overview
This project demonstrates the implementation of Slowly Changing Dimension 1 (SCD1) in a data integration scenario, designed and implemented as a Python-based ETL pipeline using Pandas and SQLAlchemy. SCD1 is a common technique used in data warehousing to handle historical changes in dimension data. In this example, we focus on maintaining historical product information in a Microsoft SQL Server database.

### Key Components
* Data Extraction: Utilizes Pandas to read data from a CSV file ('products.txt') and SQLAlchemy to query an existing SQL Server table ('product_p1').

* Data Transformation: Merges the extracted and database data using Pandas, identifying new records for insertion and existing records for update.This step simulates the 
  SCD1 process.

* Staging Area: Creates a staging table ('products_stg') to hold the updated records before applying changes to the main dimension table.

* Update Operation: Executes SQL update statements to synchronize the main dimension table ('product_p1') with the staged changes.

#### Usage
* Extract Data: Run the extract() function to read data from the CSV file and SQL database using Pandas and SQLAlchemy.

* Transform Data: Execute the transform() function to identify new records for insertion and existing records for update using Pandas.

* Load Staging: Use the load_staging() function to load the updates into the staging area (products_stg) using SQLAlchemy.

* Apply Updates: Run the updates() function to update the main dimension table (product_p1) with changes from the staging area using SQLAlchemy.

* Load Insert: Apply new records to the main dimension table using the load_insert() function with SQLAlchemy.


#### Here you can see Code File: [File Link](ETL-SCD1.ipynb).

