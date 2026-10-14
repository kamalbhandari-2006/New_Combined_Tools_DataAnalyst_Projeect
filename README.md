# Customer Shopping Behavior Analysis

An end-to-end data analytics portfolio project exploring customer
shopping behavior using **Python, Microsoft SQL Server, and Power BI**.
The project follows a business-focused workflow: understand the data,
clean and prepare it, answer business questions with SQL, and
communicate findings through an interactive dashboard.

> **Database note:** The tutorial uses PostgreSQL. This project uses
> **Microsoft SQL Server (T-SQL)** instead. The analytics workflow and
> business questions remain the same; database connection steps and some
> SQL syntax differ.

## Table of Contents

-   [Project Overview](#project-overview)
-   [Business Problem](#business-problem)
-   [Objectives](#objectives)
-   [Tools and Technologies](#tools-and-technologies)
-   [Dataset](#dataset)
-   [Project Workflow](#project-workflow)
-   [Business Questions](#business-questions)
-   [Dashboard](#dashboard)
-   [Key Analysis Areas](#key-analysis-areas)
-   [Repository Structure](#repository-structure)
-   [How to Run the Project](#how-to-run-the-project)
-   [SQL Server vs PostgreSQL](#sql-server-vs-postgresql)
-   [Skills Demonstrated](#skills-demonstrated)
-   [Limitations](#limitations)
-   [Acknowledgements](#acknowledgements)
-   [Author](#author)

## Project Overview

Retail businesses collect customer data to understand purchasing
patterns, product preferences, discount usage, customer satisfaction,
and subscription behavior. This project uses a customer shopping
behavior dataset to explore these areas and present useful business
insights.

The workflow covers:

1.  Understanding and exploring the raw dataset in Python.
2.  Cleaning data and preparing analysis-ready fields.
3.  Loading the prepared data into Microsoft SQL Server.
4.  Answering business questions using SQL queries.
5.  Connecting Power BI to the SQL Server data and building an
    interactive dashboard.
6.  Documenting the analysis for a portfolio.

## Business Problem

A retail business wants to understand how customers shop and what
factors are associated with purchasing behavior. The analysis focuses on
questions such as:

-   Which customer groups contribute the most revenue?
-   How do purchase amounts vary across product categories?
-   How are discounts used across products and customer segments?
-   How do subscription status and shipping type relate to spending?
-   Which products receive higher review ratings?
-   How do shopping patterns differ across age groups?

The goal is to turn raw customer data into clear, evidence-based
observations that can support decisions about marketing, customer
engagement, product strategy, and the shopping experience.

## Objectives

-   Inspect and understand the dataset before analysis.
-   Identify and handle missing values appropriately.
-   Standardize column names for easier analysis across tools.
-   Create useful analytical features, such as age groups and numeric
    purchase-frequency values, where appropriate.
-   Use SQL to answer business questions and aggregate results.
-   Build an interactive Power BI dashboard with key metrics and
    customer/product breakdowns.
-   Communicate results in a clear, business-oriented format.

## Tools and Technologies

  -----------------------------------------------------------------------
  Tool                                Purpose
  ----------------------------------- -----------------------------------
  Python                              Data inspection, cleaning,
                                      transformation, and exploratory
                                      data analysis

  pandas                              Data manipulation and preparation

  Jupyter Notebook                    Interactive analysis and
                                      documentation

  Microsoft SQL Server                Data storage and business analysis
                                      using T-SQL

  SQL Server Management Studio (SSMS) Database management and SQL query
                                      execution

  Power BI                            Interactive dashboard and data
                                      visualization

  Git and GitHub                      Version control and project
                                      portfolio
  -----------------------------------------------------------------------

## Dataset

**Dataset:** `customer_shopping_behavior.csv`

The dataset contains customer shopping information, including fields
such as:

-   Customer ID
-   Age and gender
-   Item purchased and product category
-   Purchase amount
-   Location
-   Size and color
-   Season
-   Review rating
-   Subscription status
-   Shipping type
-   Discount and promotional-code usage
-   Previous purchases
-   Payment method
-   Purchase frequency

The exact columns available depend on the supplied version of the
dataset. Review the source file and notebook before running the
workflow.

## Project Workflow

### 1. Business Understanding

Defined the retail business questions to be investigated and identified
the customer, product, spending, discount, and satisfaction measures
needed for analysis.

### 2. Data Understanding and Exploratory Data Analysis --- Python

Used pandas to load and inspect the CSV file. The exploratory analysis
included checking:

-   Dataset dimensions and column names
-   Data types and summary statistics
-   Missing values
-   Duplicate records, where relevant
-   Distributions of numeric and categorical columns

### 3. Data Cleaning and Feature Engineering --- Python

Prepared the data for reliable analysis by:

-   Standardizing column names (for example, using lowercase
    snake_case).
-   Reviewing missing values and handling them based on the relevant
    column and context.
-   Creating useful features, such as age groups and a numeric
    representation of purchase frequency, where appropriate.
-   Checking for redundant fields before removing any duplicated
    information.
-   Verifying the cleaned dataset before loading it into SQL Server.

For review ratings, a category-level median can be used to fill missing
values when that approach is appropriate for the dataset. Cleaning
decisions should be documented and validated rather than applied
blindly.

### 4. Data Loading and Business Analysis --- Microsoft SQL Server

Loaded the prepared data into Microsoft SQL Server and used T-SQL to
investigate the business questions. The analysis includes aggregations,
filtering, grouping, subqueries, conditional logic, and comparisons
across customer and product segments.

### 5. Interactive Dashboard --- Power BI

Connected Power BI to the SQL Server database and developed an
interactive dashboard to summarize customer behavior. The dashboard
focuses on key performance indicators and breakdowns by customer
segment, category, age group, subscription status, and shipping type.

### 6. Reporting and Communication

Organized the workflow and findings so that another person can
understand the business problem, reproduce the analysis, and interpret
the dashboard. Screenshots, a project report, and a presentation can be
included in the repository if available.

## Business Questions

The SQL analysis is designed to answer questions such as:

1.  **Revenue by gender:** How does total purchase amount differ across
    gender groups?
2.  **Discount behavior:** Which customers used discounts while spending
    above the overall average?
3.  **Product ratings:** Which products have the highest average review
    ratings?
4.  **Shipping comparison:** How does average purchase amount compare
    between standard and express shipping?
5.  **Subscription behavior:** How do customer count, average purchase
    amount, and total revenue differ by subscription status?
6.  **Discount reliance:** Which products have the highest proportion of
    purchases involving discounts?
7.  **Category performance:** Which product categories contribute the
    most purchase revenue and customer purchases?
8.  **Age-group analysis:** How do spending and purchase counts vary
    across age groups?
9.  **Customer shopping patterns:** How do purchase frequency, payment
    method, and other available attributes vary across customer
    segments?

The exact query logic and final conclusions should be checked against
the SQL scripts and dashboard included in this repository.

## Dashboard

The Power BI report is intended to provide a quick overview of customer
shopping behavior, with visuals such as:

-   KPI cards for customer count, average purchase amount, and average
    review rating
-   Subscription-status distribution
-   Revenue by product category
-   Purchase/customer counts by category
-   Revenue and purchase counts by age group
-   Interactive slicers for fields such as subscription status, gender,
    category, and shipping type

**Dashboard preview:** Add a screenshot of your actual dashboard to the
repository and update the path below.

``` markdown
![Customer Shopping Behavior Dashboard](images/customer_behavior_dashboard.png)
```

If your screenshot is saved under a different name or folder, update the
image path accordingly. GitHub will display the preview once the image
is committed to the repository.

## Key Analysis Areas

### Customer Behavior

-   Compare purchasing behavior across customer segments.
-   Explore subscription status and purchase frequency.
-   Review differences across age groups and gender.

### Product and Category Performance

-   Compare total purchase amount across categories.
-   Identify products with higher average review ratings.
-   Examine how product preferences vary by customer segment.

### Discounts and Promotions

-   Explore discount usage across products and customer groups.
-   Compare discounted purchases with the overall average purchase
    amount.
-   Investigate whether discount usage is concentrated in particular
    products.

### Shipping and Customer Experience

-   Compare average purchase amount by shipping type.
-   Explore review ratings and other available customer-experience
    indicators.

## Repository Structure

A suggested structure is shown below. Adjust the names to match the
files you actually upload.

``` text
customer-shopping-behavior-analysis/
│
├── data/
│   └── customer_shopping_behavior.csv
│
├── notebooks/
│   └── customer_behavior_analysis.ipynb
│
├── sql/
│   └── customer_behavior_analysis.sql
│
├── powerbi/
│   └── customer_behavior_dashboard.pbix
│
├── images/
│   └── customer_behavior_dashboard.png
│
├── reports/
│   └── project_report.pdf
│
└── README.md
```

Only include files and folders that exist in your repository. If you do
not have a separate `data`, `reports`, or `images` folder, remove that
entry or change it to match your actual layout.

## How to Run the Project

### Prerequisites

-   Python 3.x
-   Jupyter Notebook or JupyterLab
-   pandas and any other libraries imported by your notebook
-   Microsoft SQL Server
-   SQL Server Management Studio (SSMS), or another SQL client
-   Power BI Desktop

### Step 1: Get the project files

Clone the repository:

``` bash
git clone <your-repository-url>
cd customer-shopping-behavior-analysis
```

Alternatively, download the repository as a ZIP file from GitHub.

### Step 2: Prepare the Python environment

Install the packages required by your notebook. At minimum, the analysis
commonly uses pandas:

``` bash
pip install pandas jupyter
```

Install any additional packages imported by your own notebook.

### Step 3: Run the Python analysis

Open the notebook in Jupyter and update the CSV file path so that it
matches your local folder structure. Run the cells in order to inspect,
clean, and prepare the dataset.

### Step 4: Set up SQL Server

1.  Open SQL Server Management Studio.
2.  Connect to your SQL Server instance.
3.  Create a database for the project.
4.  Run the SQL script included in the repository, after checking the
    table and column names.
5.  Confirm that the imported data matches the prepared dataset.

The database name, table name, and import method should match the SQL
script you upload.

### Step 5: Open the Power BI dashboard

1.  Open the `.pbix` file in Power BI Desktop.
2.  If prompted, update the SQL Server server and database connection
    details.
3.  Refresh the data.
4.  Confirm that the visuals and slicers work as expected.

Do not upload database passwords or other credentials to GitHub. Use
your own local connection settings.

## SQL Server vs PostgreSQL

The tutorial demonstrates PostgreSQL, while this project uses Microsoft
SQL Server. This is a database-platform difference, not a change to the
overall project objective.

  -----------------------------------------------------------------------
  Area                    PostgreSQL tutorial     This project
  ----------------------- ----------------------- -----------------------
  Database                PostgreSQL              Microsoft SQL Server

  Query language          PostgreSQL SQL          T-SQL

  Common database client  pgAdmin                 SQL Server Management
                                                  Studio (SSMS)

  Python connection       Often `psycopg2` /      Commonly `pyodbc` /
                          SQLAlchemy              SQLAlchemy

  Power BI connector      PostgreSQL database     SQL Server database
                          connector               connector
  -----------------------------------------------------------------------

Some syntax may need to change between database systems. For example,
PostgreSQL commonly uses `LIMIT` to restrict rows, while SQL Server uses
`TOP` or `OFFSET ... FETCH`. String, date, type-conversion, and
connection syntax can also differ.

The business questions and analysis goals remain broadly the same, but
queries should be written and tested for SQL Server.

## Skills Demonstrated

-   Python data analysis with pandas
-   Data inspection, cleaning, and feature engineering
-   Exploratory data analysis (EDA)
-   SQL querying and business-focused analysis
-   Aggregations, filtering, grouping, subqueries, and conditional logic
-   Microsoft SQL Server and T-SQL
-   Power BI dashboard development
-   KPI visualization and interactive filtering
-   Translating analytical questions into measurable business questions
-   Documenting and presenting an end-to-end analytics workflow

## Limitations

-   The dataset represents the fields available in the supplied file; it
    may not contain complete transaction histories for each customer.
-   Relationships found in this analysis are descriptive and should not
    automatically be interpreted as causal.
-   Business recommendations should be based on the actual query outputs
    and dashboard results, not assumptions.
-   Results can differ if the source dataset or cleaning steps differ.

## Acknowledgements

This project was developed as a learning and portfolio exercise inspired
by the end-to-end workflow demonstrated in:

**"COMPLETE Data Analytics Portfolio Project in 6 EASY Steps \| Python +
SQL + Power BI" --- Amlan Mohanty**

-   [YouTube tutorial](https://www.youtube.com/watch?v=5PrZvPeUw60)
-   [Reference project repository and
    dataset](https://github.com/amlanmohanty1/customer-trends-data-analysis-SQL-Python-PowerBI)

The database implementation in this version uses **Microsoft SQL
Server** instead of PostgreSQL.

## Author

**Kamal Bhandari**

-   GitHub: [kamalbhandari-2006](https://github.com/kamalbhandari-2006)

------------------------------------------------------------------------

If you find this project useful, feel free to explore the repository and
review the notebook, SQL queries, and Power BI dashboard.
