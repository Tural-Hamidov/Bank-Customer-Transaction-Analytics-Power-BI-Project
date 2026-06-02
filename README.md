# Bank-Customer-Transaction-Analytics-Power-BI-Project
A Power BI banking analytics dashboard project focused on customer segmentation, account portfolio analysis, transaction trends, KPI monitoring, frozen account tracking, and risk-level evaluation through an interactive multi-page reporting solution.

# Bank Customer & Transaction Analytics - Power BI Dashboard

## 🏦 Project Overview

This project analyzes banking data to understand customer behavior, account status distribution, transaction trends, and high-risk financial activity.

The dashboard is designed to help bank management monitor key performance indicators, understand customer segments, evaluate the account portfolio, and track high-value transactions through an interactive multi-page reporting solution.

The analysis mainly focuses on:

- customer segmentation
- account status analysis
- transaction behavior
- high-value transaction monitoring
- risk level analysis
- frozen account monitoring
- KPI-based decision support for management

---

## 🗂️ Dataset Overview

The project uses 3 related datasets:

| Dataset | Description |
|---|---|
| `customers.csv` | Customer information such as name, birth date, city, income, and join date |
| `accounts.csv` | Account information such as account type, balance, status, and customer ID |
| `transactions_bank.csv` | Transaction information such as transaction date, type, amount, account ID, and description |

These datasets were connected through customer and account IDs to build a unified analytical data model.

---

## 🎯 Objectives

The main objectives of this project were to:

- build a proper data model in Power BI
- connect customer, account, transaction, and date tables
- prepare and clean raw CSV files using Power Query
- create customer, balance, transaction, and risk-based segments
- calculate key KPIs using DAX measures
- design a 4-page interactive dashboard
- generate customer, account, transaction, and risk-related insights
- identify risky transactions more efficiently
- create a clear management-oriented reporting solution

---

## 🧹 Data Preparation

Data preparation was mainly completed in **Power Query** before building the dashboard visuals.

Power Query was used as the main data cleaning and transformation layer to prepare the raw CSV files for analysis.

The main preparation steps included:

- imported `customers.csv`, `accounts.csv`, and `transactions_bank.csv` into Power BI
- cleaned and prepared the datasets in **Power Query**
- corrected data types for ID, date, text, balance, income, and transaction amount columns
- checked and adjusted date fields such as customer birth date, join date, and transaction date
- ensured customer, account, and transaction tables were ready for relationship modeling
- prepared clean query outputs before loading the data into the Power BI model
- applied **Close & Apply** to load the cleaned data into the report model
- created a separate Date Table for time-based transaction analysis
- built relationships between customers, accounts, transactions, and the Date Table
- created additional analytical fields such as customer age, age group, income group, balance group, transaction size, and risk level
- organized key KPI measures inside a separate Measures Table

Using Power Query before modeling helped make the dataset cleaner, more consistent, and ready for reliable dashboard analysis.

---

## 🔗 Data Model

The model was built using the following relationship logic:

| Relationship | Cardinality |
|---|---|
| Customers → Accounts | One-to-Many |
| Accounts → Transactions | One-to-Many |
| Date Table → Transactions | One-to-Many |

This model allows customer-level, account-level, transaction-level, and time-based analysis within one connected report.

---

## 📊 Dashboard Pages

The dashboard consists of 4 main pages:

### 1. Overview

Provides a high-level summary of the bank portfolio.

Includes:

- total balance
- customer count
- account count
- total transactions
- risk transaction ratio
- customers by city
- account type distribution
- account status distribution
- monthly transaction trend

<p align="center">
  <img src="assets/overview.png" alt="Overview Dashboard" width="100%">
</p>

---

### 2. Customer Analysis

Focuses on customer segmentation and profile analysis.

Includes:

- customers by age group
- customers by city
- customers by income group
- balance by income group
- customer details table

<p align="center">
  <img src="assets/customer-analysis.png" alt="Customer Analysis Dashboard" width="100%">
</p>

---

### 3. Transaction Analysis

Analyzes transactions by date, type, size, and amount.

Includes:

- monthly transaction amount trend
- transactions by type
- transaction size distribution
- average amount by transaction type
- top transactions table

<p align="center">
  <img src="assets/transaction-analysis.png" alt="Transaction Analysis Dashboard" width="100%">
</p>

---

### 4. Risk Monitoring

Designed to monitor risky transactions and frozen accounts.

Includes:

- frozen accounts
- high-risk transactions
- critical-risk transactions
- risk ratio
- risk level distribution
- critical risk by transaction type
- risk transaction details table

<p align="center">
  <img src="assets/risk-monitoring.png" alt="Risk Monitoring Dashboard" width="100%">
</p>

---

## 📌 KPI Snapshot

| KPI | Value |
|---|---:|
| Total Balance | 300.69K |
| Customer Count | 100 |
| Account Count | 55 |
| Total Transactions | 194 |
| Total Transaction Amount | 973.05K |
| Frozen Accounts | 26 |
| Critical Risk Transactions | 97 |
| High Risk Transactions | 38 |
| Risk Transaction Ratio | 69.59% |

---

## 🔍 Key Findings

The dashboard provides a clear view of the bank’s customer base, account portfolio, transaction behavior, and risk indicators. It allows management to analyze customer segments, transaction activity, and risky accounts or transactions within a single report.

### 1. Customer Base Structure

The customer distribution shows that the bank’s customer base is spread across different cities. The highest number of customers is observed in **Lankaran**, indicating that this region has a relatively active and important customer base for the bank.

Age group analysis shows that customers are mainly concentrated in young and working-age segments. These groups can be valuable for the bank because they are more likely to actively use daily banking services, card products, loans, and digital banking channels.

For income analysis, customers were grouped by income level. Customers with `income = 0` were separated into an **Unknown Income** group. This approach keeps known-income customers separate from customers whose income is not clearly available or is recorded as zero, making income segmentation cleaner and easier to interpret.

### 2. Account Portfolio and Status Analysis

The account data was analyzed across Current, Savings, and Credit account types. This distribution helps evaluate the bank’s product portfolio.

Account status analysis shows that accounts are grouped into **Active**, **Closed**, and **Frozen** statuses. The **Frozen Accounts** KPI is especially important from an operational and risk monitoring perspective.

Frozen accounts should not be treated only as a passive metric. They may require additional attention due to:

- transaction restrictions
- compliance or risk control processes
- unusual account activity
- internal banking procedures
- ongoing customer/account review processes

Monitoring frozen accounts separately can help strengthen operational control and risk visibility.

### 3. Transaction Behavior

The Transaction Analysis page shows how transactions are distributed by time, type, and amount. According to the dashboard, the total number of transactions is **194**, while the total transaction amount is **973.05K**.

Transaction type analysis shows that Transfer, Deposit, and Withdrawal are the main transaction categories. In terms of average transaction amount, **Transfer** transactions appear to be higher. This suggests that transfer operations are more closely related to larger money movements.

The Transaction Size Distribution indicates that high-value transactions represent a significant part of the overall transaction structure. These transactions may be valuable from a business perspective, but they also require closer monitoring from a risk perspective.

### 4. Risk Indicators

The Risk Monitoring page was created to track transactions by risk level. The risk level is used as an initial monitoring indicator based on transaction amount.

According to the dashboard:

| Indicator | Value |
|---|---:|
| Critical Risk Transactions | 97 |
| High Risk Transactions | 38 |
| Risk Transaction Ratio | 69.59% |

This shows that a significant share of analyzed transactions falls into high-risk and critical-risk categories. This does not mean that these transactions are confirmed fraud. Instead, they should be treated as priority transactions for additional monitoring.

Critical-risk transactions are mostly observed in **Transfer** operations. Since transfers often represent high-value money movements, they should be monitored more carefully by risk and compliance teams.

### 5. Management Perspective

The dashboard creates value for bank management in four main areas:

- better understanding of customer segments
- operational monitoring of account statuses
- analysis of transaction volume and behavior
- early identification of high-risk transactions

This report is not only a visual dashboard, but also an analytical tool that supports decision-making in customer analytics, operational control, and risk monitoring.

---

## 💡 Business Recommendations

Based on the analysis, the following business recommendations can be made.

### 1. Create a Separate Monitoring Process for Frozen Accounts

Tracking frozen accounts as a separate KPI can improve the bank’s operational and risk control. These accounts should be analyzed periodically and grouped by the reason for their frozen status.

Recommended actions:

- monitor frozen account counts weekly and monthly
- analyze frozen accounts by account type and city
- prioritize frozen accounts with high balances
- categorize reasons for frozen status
- investigate accounts that remain frozen for a long period

This approach can improve both risk control and operational transparency.

### 2. Prioritize High-Value Transfer Transactions

The dashboard shows that critical-risk transactions are mostly observed in Transfer operations. Therefore, transfers should be treated as a priority area in risk monitoring.

The bank can apply the following control mechanisms:

- automatic alerts for high-value transfers
- monitoring repeated large transfers from the same account
- detecting multiple high-value transactions within a short time period
- analyzing transfer transactions together with account status
- adding critical-risk transfers to a dedicated review list

This approach can help risk teams focus on the most important transactions more efficiently.

### 3. Use the Risk Monitoring Page as a Daily Control Panel

The Risk Monitoring page can work as an early warning dashboard for the bank. It brings risky transactions, frozen accounts, and critical activities into one view.

Possible use cases:

- daily risk overview
- monitoring high-risk and critical-risk transactions
- reviewing transaction distribution by risk level
- investigating transactions related to frozen accounts
- preparing priority lists for the risk team

This can help the bank move from reactive risk management to a more proactive monitoring approach.

### 4. Use Customer Segmentation in Business Strategy

The Customer Analysis page allows customers to be analyzed by age, city, and income group. These segments can support sales, marketing, and product strategy.

Possible applications:

- digital banking and card campaigns for younger customers
- loan and savings products for working-age customers
- premium services for high-income customers
- region-based local campaigns
- branch and service strategy based on city-level customer activity

This approach can help the bank make product offerings more targeted and effective.


### 5. Create Prioritization Rules for Risky Transactions

Analyzing all risky transactions at the same level is not efficient. The bank can prioritize transactions based on risk level, transaction type, account status, and balance behavior.

Example prioritization logic:

| Priority | Condition |
|---|---|
| Very High | Critical Risk + Frozen Account |
| High | Critical Risk + Transfer |
| Medium-High | High Risk + High-balance account |
| Medium | Repeated high-value transactions |

This prioritization can help risk teams focus faster on the most important cases.

### 6. Use the Dashboard as a Periodic Management Report

This dashboard can be used not only as a project deliverable, but also as a periodic management reporting tool in a real business environment.

Recommended reporting formats:

- weekly risk overview
- monthly transaction performance report
- customer segmentation report
- account status monitoring report
- KPI review panel for management

This can reduce manual reporting effort and support faster decision-making.

### 7. An account portfolio balance growth strategy can be developed

The dashboard allows the bank to analyze its account portfolio by account type, balance group, customer segment, and transaction behavior. Based on these insights, the bank can go beyond simply monitoring the current portfolio and develop a strategy focused on increasing account balances and improving customer value.

The main purpose of this business recommendation is to identify low-balance but active customers and convert them into higher-value banking customers.

Recommended actions:

- offer savings products to low-balance customers with active transaction behavior
- provide cashback, loyalty, or premium card campaigns to customers with high transaction activity
- encourage Current account users to adopt Savings accounts or additional banking products
- create personalized service and premium banking offers for high-balance customers
- design different product offers based on the combination of balance group and income group
- monitor balance performance by account type to identify underperforming product categories

This approach can make the bank’s account portfolio management more effective. The bank can better understand which account types hold higher balances, which customer groups have stronger growth potential, and which segments are more suitable for cross-sell opportunities.

As a result, the dashboard can support not only risk and transaction monitoring, but also business decisions related to balance growth, cross-selling, and customer value improvement.

---


## 🏁 Conclusion

In this Power BI project, raw banking data was transformed into an interactive and management-ready dashboard.

As part of the project, customer data, account data, and transaction data were prepared, cleaned, and structured for analysis using **Power Query**. After the data preparation stage, proper relationships were built between the tables, a Date Table was created, and DAX measures were used to calculate the main KPIs.

The final dashboard allows banking activity to be analyzed from several key perspectives:

- customer analysis by city, age group, and income group
- monitoring of account types, balances, and account statuses
- transaction analysis by time, type, amount, and size
- separate tracking of frozen accounts
- identification of high-risk and critical-risk transactions
- KPI-based overview for management-level decision-making

One of the main strengths of the project is the dedicated **Risk Monitoring** page. This page makes it easier to track risky transactions, frozen accounts, and critical financial activity in one place. As a result, the dashboard can be used not only as a visual report, but also as an analytical tool that supports risk and operational monitoring.

The project fully meets the case study requirements and was extended with a fourth dashboard page, page navigation, bookmarks, slicers, and business-oriented insights.

Overall, this project demonstrates how banking data can be cleaned, modeled, analyzed, and presented as a professional Power BI dashboard. The final report supports customer analysis, account portfolio monitoring, transaction tracking, and risk-based decision-making.

