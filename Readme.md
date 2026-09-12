# Customer Behaviour Analysis

An end-to-end customer behaviour analysis project using Python, MySQL, SQL, and Power BI. The project prepares raw customer shopping data, extracts business insights, and presents findings through an interactive dashboard.

## Project Overview

This project analyzes customer purchasing behaviour to identify patterns related to:

- Customer segments
- Purchase frequency
- Spending behaviour
- Discounts and promotions
- Customer loyalty
- Product categories
- Review ratings
- Purchase drivers

## Deliverables

### 1. Data Preparation and Modeling — Python

The raw dataset is cleaned and transformed using Pandas.

Key tasks include:

- Loading the customer shopping dataset
- Inspecting data types and missing values
- Filling missing review ratings using category-level medians
- Standardizing column names
- Creating age groups
- Converting purchase frequency into days
- Removing duplicate information
- Exporting the prepared dataset to MySQL

### 2. Data Analysis — SQL

The cleaned data is loaded into MySQL for structured analysis.

SQL analysis focuses on:

- Customer segmentation
- Spending patterns
- Purchase frequency
- Customer loyalty
- Discount usage
- Product category performance
- Review ratings
- Customer purchase drivers

### 3. Visualization and Insights — Power BI

An interactive Power BI dashboard is used to communicate the findings.

The dashboard highlights:

- Key performance indicators
- Customer demographics
- Category-level trends
- Purchase frequency
- Spending behaviour
- Discount and subscription patterns
- Customer loyalty insights

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- MySQL
- SQLAlchemy
- PyMySQL
- Power BI
- Jupyter Notebook

## Dataset

The project uses a customer shopping behaviour dataset stored as:

`customer_shopping_behavior.csv`

## Project Structure

```text
Customer_behaviour_analysis/
│
├── Behaviour_analysis.ipynb
├── customer_shopping_behavior.csv
├── README.md
├── SQL/
│   └── customer_analysis.sql
└── PowerBI/
    └── customer_behaviour_dashboard.pbix
```

> Update the folder and file names above if they differ in the repository.

## How to Import and Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/shubhankhiremath/Customer_behaviour_analysis.git
cd Customer_behaviour_analysis
```

### 2. Create a virtual environment

On Windows:

```bash
python -m venv venv
venv\Scripts\activate
```

### 3. Install the required Python packages

```bash
pip install pandas numpy matplotlib seaborn sqlalchemy pymysql jupyter
```

### 4. Open the Jupyter Notebook

```bash
jupyter notebook Behaviour_analysis.ipynb
```

Run the notebook cells in order to clean and prepare the dataset.

## MySQL Configuration

Create a MySQL database:

```sql
CREATE DATABASE Customer_DB;
```

Update the database connection details in the notebook:

```python
from sqlalchemy import create_engine
from sqlalchemy.engine import URL

connection_url = URL.create(
    "mysql+pymysql",
    username="your_username",
    password="your_password",
    host="localhost",
    port=3306,
    database="Customer_DB"
)

engine = create_engine(connection_url)
```

The prepared data is loaded into a MySQL table named:

```text
customers
```

For security, do not commit real database passwords to GitHub. Use environment variables or a local configuration file instead.

## Power BI Dashboard

To view the dashboard:

1. Open Power BI Desktop.
2. Open the `.pbix` file from the `PowerBI` folder.
3. Refresh the data connection if required.
4. Review the interactive visualizations and filters.

## Key Outcomes

This project demonstrates how to:

- Prepare raw data for analysis
- Transform and enrich customer data
- Load data into a relational database
- Use SQL to answer business questions
- Build an interactive Power BI dashboard
- Convert customer data into actionable business insights

## Author

**Shubhank Hiremath**

GitHub: [Customer Behaviour Analysis](https://github.com/shubhankhiremath/Customer_behaviour_analysis)