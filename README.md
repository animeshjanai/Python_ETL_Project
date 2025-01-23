# Python ETL Project: Currency Conversion and Expense Management

## Overview
This project demonstrates an **ETL (Extract, Transform, Load)** process using Python. The goal is to manage expenses in **USD**, convert them to **CAD** (Canadian Dollars) using live exchange rates, and store the data in an **SQL Server database**.

---

## Features
- Fetches real-time exchange rates from the **Bank of Canada** API.
- Reads and processes an **Excel file** containing expense data.
- Converts expenses from **USD** to **CAD**.
- Stores the processed data in an **SQL Server database**.

---

## Project Structure
1. **`etl.ini`**: Configuration file containing settings like:
   - Start date for exchange rate data.
   - Bank of Canada API URL.
   - SQL Server details (server name, database name).

2. **SQL Script**: Prepares the database and table:
   - Creates a database named `ETLDemo`.
   - Creates a table named `Expenses` to store the final data.

3. **Excel File**: Contains the raw expense data (`date` and `USD` columns).

4. **Python Code**: Handles the entire ETL process:
   - **Extract**: Fetches exchange rates from the API and loads the Excel file.
   - **Transform**: Joins the data, calculates **CAD** amounts, and cleans the data.
   - **Load**: Inserts the final data into the `Expenses` table in SQL Server.
