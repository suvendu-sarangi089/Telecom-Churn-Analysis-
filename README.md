# Customer Churn Analysis 📊

An exploratory data analysis (EDA) project on telecom customer churn, aimed at identifying the key factors that drive customers to leave the service.

## 📌 Project Overview

Customer churn — when a customer stops doing business with a company — is one of the most expensive problems a subscription-based business can face. Acquiring a new customer typically costs far more than retaining an existing one, which makes understanding *why* customers leave a high-value business question.

This project analyzes a dataset of **7,043 telecom customers** to uncover patterns behind churn behavior, using data cleaning, statistical checks, and visual exploratory analysis.

## 🎯 Objective

- Clean and prepare raw customer data for analysis
- Identify data quality issues (missing values, incorrect data types, duplicates)
- Explore the distribution of key numerical features (tenure, monthly charges, total charges)
- Analyze how categorical features (contract type, internet service, payment method, etc.) relate to churn
- Extract actionable business insights to help reduce customer churn

## 🗂️ Dataset

- **Source:** Telecom customer records
- **Rows:** 7,043 customers
- **Columns:** 21 features, including demographic info, account details, subscribed services, and churn status
- **Target variable:** `Churn` (Yes/No)

## 🧹 Data Cleaning

- Removed the `customerID` column (a unique identifier with no analytical value)
- Converted `TotalCharges` from text to numeric type using `pd.to_numeric()`
- Identified and handled 11 missing values in `TotalCharges`, all belonging to customers with 0 months tenure (new customers not yet billed); resolved by filling with 0
- Identified and corrected a binning issue in a derived `Tenure_Group` feature that excluded `tenure = 0` customers, using `include_lowest=True`
- Checked for and investigated 22 duplicate rows (identified only after removing the unique `customerID` column)
- Verified no statistical outliers in `tenure`, `MonthlyCharges`, or `TotalCharges` using the IQR method

## 📈 Exploratory Data Analysis

- Univariate analysis of numerical features (histograms with KDE)
- Churn rate distribution across the full customer base
- Bivariate analysis: numerical and categorical features vs. Churn
- Correlation heatmap of numerical variables

## 🔍 Key Insights

*(To be filled in as you complete each analysis step — e.g., "Customers on month-to-month contracts churn significantly more than those on 1-2 year contracts.")*

## 🛠️ Tools & Libraries

- **Python 3**
- **Pandas** — data manipulation
- **NumPy** — numerical operations
- **Matplotlib** & **Seaborn** — data visualization

## 📁 Repository Structure

```
├── CHURN_ANALYSIS.ipynb     # Main analysis notebook
├── Customer_Churn.csv       # Dataset
└── README.md                # Project documentation
```

## 🚀 How to Run

```bash
git clone <your-repo-url>
cd <repo-folder>
pip install pandas numpy matplotlib seaborn
jupyter notebook CHURN_ANALYSIS.ipynb
```

## 📬 Contact

Feel free to reach out if you have questions or suggestions about this project.

---
*This project is part of my data analysis learning portfolio.*
