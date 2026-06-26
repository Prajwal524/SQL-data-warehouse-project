# 📊 Data Warehouse and Analytics Project

A comprehensive end-to-end **Data Warehouse and Analytics** project demonstrating modern data engineering practices using **SQL Server** and the **Medallion Architecture** (Bronze, Silver, Gold). This project covers the complete data warehousing lifecycle, from ingesting raw data to building a business-ready analytical model capable of generating actionable insights.

> Designed as a portfolio project to showcase practical skills in data engineering, ETL development, data modeling, and SQL analytics.

---

## 🏗️ Data Architecture

This project follows the **Medallion Architecture**, organizing data into three logical layers.

```
                Source Systems
              (ERP & CRM CSV Files)
                       │
                       ▼
        ┌──────────────────────────┐
        │        Bronze Layer       │
        │      Raw Data Storage     │
        └──────────────────────────┘
                       │
                       ▼
        ┌──────────────────────────┐
        │        Silver Layer       │
        │ Data Cleaning & Standardization │
        └──────────────────────────┘
                       │
                       ▼
        ┌──────────────────────────┐
        │         Gold Layer        │
        │ Star Schema & Analytics   │
        └──────────────────────────┘
                       │
                       ▼
            SQL Analytics & Reporting
```

> The architecture diagram can also be found in **docs/data_architecture.drawio**.

---

## 📖 Project Overview

This project demonstrates the design and implementation of a modern SQL-based data warehouse capable of transforming raw operational data into meaningful business insights.

The solution covers:

* Designing a layered Data Warehouse using the Medallion Architecture
* Building ETL pipelines for data ingestion and transformation
* Cleaning and validating data from multiple source systems
* Integrating ERP and CRM datasets
* Designing an optimized Star Schema
* Creating analytical SQL queries for business reporting
* Producing business-ready datasets for downstream analytics

---

## 🎯 Project Objectives

* Build a scalable SQL Server Data Warehouse
* Consolidate data from multiple operational systems
* Improve data quality through cleansing and standardization
* Design an efficient dimensional data model
* Enable fast analytical querying
* Generate meaningful business insights using SQL

---

# 🏛️ Medallion Architecture

## 🥉 Bronze Layer

The Bronze layer stores raw source data exactly as received.

Features:

* Raw CSV ingestion
* No transformations
* Preserves source data
* Supports data traceability

---

## 🥈 Silver Layer

The Silver layer focuses on improving data quality.

Transformations include:

* Removing duplicate records
* Handling NULL values
* Standardizing formats
* Data type conversions
* Cleaning inconsistent values
* Basic validation rules
* Preparing integrated datasets

---

## 🥇 Gold Layer

The Gold layer contains business-ready analytical models.

Features:

* Star Schema
* Fact Tables
* Dimension Tables
* Optimized analytical queries
* Reporting-ready datasets

---

# 🛠 Technology Stack

| Category            | Technologies                        |
| ------------------- | ----------------------------------- |
| Database            | SQL Server                          |
| Query Language      | T-SQL                               |
| Database Management | SQL Server Management Studio (SSMS) |
| Architecture        | Medallion Architecture              |
| Data Modeling       | Star Schema                         |
| Source Data         | CSV Files                           |
| Version Control     | Git & GitHub                        |
| Documentation       | Markdown                            |
| Diagramming         | Draw.io                             |

---

# 📂 Repository Structure

```text
SQL-data-warehouse-project/
│
├── datasets/
│   ├── source_crm/
│   └── source_erp/
│
├── docs/
│   ├── data_architecture.drawio
│   ├── data_flow.drawio
│   ├── data_models.drawio
│   ├── etl.drawio
│   ├── data_catalog.md
│   └── naming-conventions.md
│
├── scripts/
│   ├── bronze/
│   ├── silver/
│   └── gold/
│
├── tests/
│
├── README.md
├── LICENSE
├── .gitignore
└── requirements.txt
```

---

# 🔄 ETL Pipeline

The ETL workflow follows a layered approach.

```
ERP CSV Files
              \
               \
                ---> Bronze Layer
               /
CRM CSV Files /
                    │
                    ▼
              Silver Layer
        (Cleaning & Validation)
                    │
                    ▼
              Gold Layer
          (Star Schema Model)
                    │
                    ▼
        SQL Analytics & Reporting
```

---

# 📦 Data Sources

The warehouse integrates data from two independent operational systems.

### ERP System

Provides enterprise resource planning data such as:

* Products
* Sales
* Categories
* Product Information

### CRM System

Provides customer relationship management data including:

* Customer Information
* Customer Demographics
* Sales Transactions

These datasets are merged into a unified analytical model for reporting and business intelligence.

---

# ⭐ Data Modeling

The Gold Layer is designed using a **Star Schema**, separating business entities into:

### Fact Tables

Contain measurable business events such as:

* Sales
* Revenue
* Quantity

### Dimension Tables

Provide descriptive business context including:

* Customers
* Products
* Categories
* Dates

This structure improves query performance while simplifying analytical reporting.

---

# 📈 Analytics & Reporting

The project includes SQL-based analytics covering multiple business domains.

### Customer Analytics

* Customer segmentation
* Customer purchasing behavior
* High-value customers
* Customer activity trends

### Product Analytics

* Best-selling products
* Product performance
* Revenue contribution
* Category analysis

### Sales Analytics

* Revenue trends
* Monthly sales analysis
* Order performance
* Sales growth

---

# 💡 SQL Concepts Demonstrated

This project demonstrates practical SQL development using:

* SELECT Statements
* Joins
* Common Table Expressions (CTEs)
* Window Functions
* Aggregate Functions
* GROUP BY
* CASE Statements
* Views
* Stored Procedures
* Constraints
* Data Cleaning Techniques
* Data Transformation
* Data Integration
* Analytical Queries

---

# 📋 Business Requirements

The solution was developed to support business users by answering questions such as:

* Who are the highest-value customers?
* Which products generate the most revenue?
* Which product categories perform best?
* How do sales change over time?
* What are the monthly revenue trends?
* Which customers contribute the highest sales?
* Which products are underperforming?
* What insights can improve business decisions?

---

# 🚀 Getting Started

## Clone the Repository

```bash
git clone https://github.com/Prajwal524/SQL-data-warehouse-project.git
```

```bash
cd SQL-data-warehouse-project
```

---

## Requirements

* SQL Server
* SQL Server Management Studio (SSMS)
* Git
* GitHub

---

## Project Setup

1. Clone the repository.
2. Create a new SQL Server database.
3. Import the provided CSV datasets.
4. Execute the scripts in the following order:

```
Bronze
   ↓
Silver
   ↓
Gold
```

5. Run the analytical SQL queries.

---

# 📚 Learning Outcomes

This project demonstrates experience with:

* Modern Data Warehouse Design
* ETL Development
* SQL Data Engineering
* Data Cleansing
* Data Integration
* Data Modeling
* Star Schema Design
* Business Analytics
* SQL Reporting
* Database Documentation
* Version Control using Git

---

# 📁 Documentation

Additional project documentation is available inside the **docs** directory.

Included documentation:

* Data Architecture
* Data Flow
* ETL Design
* Data Model
* Naming Conventions
* Data Catalog

---

# 🔮 Future Improvements

Potential enhancements include:

* Incremental Data Loading
* Slowly Changing Dimensions (SCD Type 2)
* Automated ETL Scheduling
* Data Quality Validation Framework
* Power BI Dashboards
* Azure Data Factory Integration
* Cloud Data Warehouse Deployment
* CI/CD Pipeline Integration
* Data Lineage Tracking

---

# 🤝 Contributing

Contributions, suggestions, and improvements are welcome.

If you'd like to improve this project:

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Open a Pull Request

---

# 📬 Contact

**Prajwal Y**

📧 Email: [prajuacharya2004@gmail.com](mailto:prajuacharya2004@gmail.com)

💼 LinkedIn: https://www.linkedin.com/in/prajwal-y524/

🐙 GitHub: https://github.com/Prajwal524

---

## ⭐ Support

If you found this project helpful or informative, consider giving the repository a **Star ⭐**. Your support helps increase the visibility of the project and encourages future improvements.

---

## 📄 License

This project is licensed under the **MIT License**.

You are free to use, modify, and distribute this project with appropriate attribution.
