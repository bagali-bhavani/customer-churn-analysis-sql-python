# Customer Churn Analysis using SQL and Python

## Project Overview
This project analyzes customer churn using SQLite, SQL, and Python. It covers database extraction, data cleaning, feature engineering, KPI analysis, and churn-focused exploratory analysis to identify retention risks and business improvement opportunities.

---

## Business Problem
Customer churn directly impacts recurring revenue and long-term customer value. The objective of this project is to identify customer and subscription patterns associated with churn and provide data-driven insights that can support customer retention strategies.

---

## Objectives
- Extract customer data from a SQLite database
- Clean and preprocess customer, subscription, and support datasets
- Perform feature engineering for churn analysis
- Calculate business KPIs related to customer churn
- Analyze churn across subscription plans and customer support behavior
- Generate business insights and recommendations

---

## Dataset Information

The project uses three relational tables stored in a SQLite database:

- `db_customer`
- `db_subscription`
- `db_support`

The data contains customer demographics, subscription details, churn information, customer complaints, escalation status, customer satisfaction score, monthly charges, customer lifetime value (CLTV), and churn score.

---

## Database Information

- **Database:** SQLite
- **Database File:** `customer_churn.db`
- **Extraction Method:** SQL queries using Python `sqlite3` and pandas

---

## Technologies Used

- Python
- SQL
- SQLite
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Project Workflow

1. Connected to the SQLite database
2. Extracted customer, subscription, and support tables
3. Cleaned and standardized data
4. Converted date columns into datetime format
5. Performed feature engineering
6. Merged datasets
7. Calculated business KPIs
8. Performed Exploratory Data Analysis (EDA)
9. Generated visualizations
10. Derived business insights and recommendations

---

## Methodology

### 1. Data Extraction
Connected to the SQLite database using Python and extracted all required tables into pandas DataFrames.

### 2. Data Cleaning

Cleaning steps included:

- Renamed `name` to `customername`
- Removed unnecessary columns (`interests`, `pincode`, `col1`, `comment`)
- Converted date columns into datetime format
- Standardized gender values
- Filled missing country values using available state-country mapping

### 3. Feature Engineering

Created the following analytical features:

- `churnflag`
- `complaintcount`
- `tenuredays`
- `churnrisk`

### 4. Data Integration

Merged customer, subscription, and support datasets into a single analysis-ready dataset.

### 5. KPI Analysis

Calculated important business metrics related to customer churn and retention.

---

## Key Performance Indicators (KPIs)

| KPI | Value |
|------|------:|
| Churn Rate | **28.57%** |
| Retention Rate | **71.43%** |
| Average Revenue Per User (ARPU) | **18.85** |
| Average Customer Tenure | **1493 Days** |
| Revenue at Risk | **73.94** |
| Escalation Rate | **19.05%** |
| Average Complaints per User | **0.43** |
| Escalation vs Churn Correlation | **0.77** |

---

## Exploratory Data Analysis

The analysis includes:

- Customer churn distribution
- Churn by subscription plan
- Customer tenure analysis
- Complaint and escalation analysis
- Churn-risk segmentation
- Revenue impact due to churn

---

## SQL Integration

SQL was used to:

- Identify available tables in the SQLite database
- Extract customer, subscription, and support data

Python was then used for:

- Data cleaning
- Feature engineering
- KPI calculation
- Data visualization
- Business analysis

---

## Visualizations

The notebook contains visualizations including:

- Customer churn distribution
- Plan-wise churn analysis
- Customer tenure analysis
- Complaint and escalation analysis
- KPI-focused charts

> Screenshots of important outputs will be added to the `images/` folder.

---

## Results

The project demonstrates an end-to-end customer churn analysis workflow using SQL and Python, covering database extraction, preprocessing, feature engineering, KPI analysis, visualization, and business interpretation.

---

## Verified Insights

- Overall churn rate is **28.57%** while retention rate is **71.43%**.
- Customers on the **Basic** subscription plan have the highest churn rate (**60.00%**).
- The **Premium** subscription plan has the lowest churn rate (**14.29%**).
- Average Revenue Per User (ARPU) is **18.85**.
- Revenue at risk due to churned customers is **73.94**.
- Escalation and churn show a strong positive correlation (**0.77**), indicating that customers with escalated support cases are more likely to churn.

---

## Business Recommendations

- Focus retention campaigns on customers using the **Basic** subscription plan.
- Resolve escalated support cases quickly to reduce customer churn.
- Monitor customers with high churn-risk scores proactively.
- Improve customer support quality and pricing strategy where necessary.
- Combine churn score, complaint history, and escalation status for early churn prediction.

---

## Project Structure

```text
customer-churn-analysis-sql-python/

├── README.md
├── requirements.txt
├── .gitignore
├── LICENSE
│
├── notebooks/
│   ├── README.md
│   └── customer_churn_analysis.ipynb
│
├── data/
│   ├── README.md
│   ├── customer_churn_raw.xlsx
│   └── customer_churn_cleaned.csv
│
├── database/
│   ├── README.md
│   └── customer_churn.db
│
├── images/
│   └── README.md
```

---

## How to Run

1. Clone this repository.
2. Install the required Python libraries:

```bash
pip install -r requirements.txt
```

3. Open `notebooks/customer_churn_analysis.ipynb`.
4. Ensure `customer_churn.db` is available inside the `database/` folder.
5. Run all notebook cells sequentially.

---

## Future Improvements

- Develop an interactive Power BI dashboard.
- Build a machine learning model for churn prediction.
- Add interactive visualizations.
- Expand the dataset with additional customer behavior metrics.
- Include more business-oriented dashboard reporting.

---

## Author

**Bhavani Bagali**

Mechanical Engineering Undergraduate  
National Institute of Technology Agartala

Aspiring Data Analyst

---

⭐ If you found this project useful, consider giving it a star.
