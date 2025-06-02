# IPL Data Integration Project (SSIS + CSV)

This project showcases the integration and transformation of IPL (Indian Premier League) data using **SQL Server Integration Services (SSIS)** and **CSV files**. It demonstrates how to build an ETL pipeline to clean, transform, and load cricket match data into a SQL Server database.

---

## 🔍 Overview

- Extract IPL match and ball-by-ball data from CSV files
- Transform the data using SSIS (data conversions, lookups, error handling)
- Load clean data into SQL Server tables
- Use Conditional Split and logging for error tracking

---

## 🛠️ Technologies Used

- SQL Server Integration Services (SSIS)
- Microsoft SQL Server
- Visual Studio with SSDT (SQL Server Data Tools)
- CSV (Comma-Separated Values) files

---

## 📂 Folder Descriptions

### `SSIS Package/`
This folder contains the full SSIS solution:
- `.sln` and `.dtproj` project files
- `.dtsx` packages implementing the ETL process
- Tasks such as:
  - Flat File Source to SQL Server Destination
  - Data Conversions and Derived Columns
  - Conditional Split for validation
  - Error redirection and logging

### `CSV Files/`
This folder contains the raw dataset files:
- `player.csv`
- `match.csv`
- Other dimension or reference files as needed

Make sure to update the flat file connection paths in SSIS to point to these files on your system.

---

## ▶️ How to Run the Project

### 1. Open the SSIS Solution
- Navigate to the `SSIS Package/` directory.
- Open the `.sln` file in **Visual Studio** (with **SSDT** installed).

### 2. Configure File Paths
- Update the file paths in all **Flat File Source** connection managers.
- Ensure they point to the correct files inside your local `CSV Files/` directory.

### 3. Execute the Package
- Run the package directly in **Visual Studio**, or
- Deploy it to your **SSIS server** for scheduled execution.

---

## 📌 Notes

- This project includes **error handling** using Conditional Split and redirects invalid rows to a separate destination (usually a flat file) for logging.
- Make sure to check and configure **all connection managers** (especially file and database paths) before running the package.
- Ensure your **SQL Server instance** is running and accessible during execution.
