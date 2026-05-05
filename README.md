# 🏦 Bank Customer Churn Analysis | SQL

---

## 📌 Project Overview

This project analyzes a dataset of **1,00,000+ bank customers** to uncover churn patterns, identify at-risk customers, and build a **Churn Risk Scorecard** using SQL. The goal is to help banks proactively retain customers before they leave.

---

## 🎯 Objectives

- Identify the overall churn rate and key churn drivers
- Analyze churn across demographics (gender, age, income, education)
- Understand behavioral patterns of churned vs retained customers
- Build a risk scoring model to flag high-risk customers

---


**Key columns used:**
`Attrition_Flag`, `Customer_Age`, `Gender`, `Income_Category`, `Card_Category`, `Credit_Limit`, `Total_Trans_Amt`, `Total_Trans_Ct`, `Months_Inactive_12_mon`, `Contacts_Count_12_mon`, `Avg_Utilization_Ratio`

---

## 🛠️ Tools Used

- **MySQL** – Data cleaning, querying, analysis
- **SQL Concepts** – Aggregations, CASE statements, Window Functions, CTEs, Subqueries

---

## 🧹 Data Cleaning Steps

| Step | Action |
|------|--------|
| Duplicate Check | No duplicates found |
| Missing Values | Flagged Unknown in Education (1,519), Marital Status (749), Income (1,112) |
| Label Standardization | Renamed `Attrited Customer` → `Churned`, `Existing Customer` → `Retained` |
| Range Validation | Verified all numeric columns fall within realistic ranges |

---

## 📊 Key Findings

| Insight | Finding |
|---------|---------|
| 📉 Overall Churn Rate | **16.07%** |
| 👩 Gender | Female churn (17.36%) > Male churn (14.62%) |
| 😴 Inactivity | More inactive months = higher churn |
| 💳 Card Type | Blue card holders churn the most |
| 📞 Bank Contacts | Customers contacting 5–6 times/year churn most |
| 🎓 Education | Doctorate holders churn the most (21.06%) |
| 👴 Age Group | Pre-Retirement (46–60) has highest churn (16.62%) |
| 🔗 Products Held | Fewer products = higher churn risk |
| 💸 Spending | Churned customers spend less and transact less |

---

## 🚨 Churn Risk Scorecard (Query 15)

Built a custom risk scoring model assigning points based on behavioral signals:

| Signal | Points |
|--------|--------|
| Inactive ≥ 3 months | +2 |
| Contacts ≥ 4 times/year | +2 |
| Products held ≤ 2 | +2 |
| Transactions ≤ 40/year | +2 |
| Utilization ratio ≤ 0.1 | +1 |
| Spend change Q4/Q1 ≤ 0.6 | +1 |

**Risk Tiers:**
- 🔴 **HIGH RISK** → Score ≥ 6
- 🟡 **MEDIUM RISK** → Score 3–5
- 🟢 **LOW RISK** → Score < 3

---

## 📁 Files in This Repository


 `bank_churn_analysis.sql` => All 15 SQL queries with comments and insights 
 `BankChurners.csv` => Raw dataset 
 `Bank_Churn_Report.docx` => Detailed project report 

---


## 👩‍💻 Author

**Masira Siddiqui**
📍 Mumbai, India
🔗 [LinkedIn](https://www.linkedin.com/in/masirasiddiqui)

---

*This project was completed as part of self-learning in Data Analytics.*
