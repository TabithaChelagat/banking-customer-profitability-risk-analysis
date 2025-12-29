# Banking Customer Profitability & Risk Monitoring

## 📌 Project Overview
This project demonstrates advanced SQL analytics in a retail banking context. It focuses on identifying high-value customers, assessing loan default risk, and detecting fraudulent transaction patterns to improve the bank's operational efficiency and risk posture.

## 📊 Business Questions Answered
1. **Who are our most valuable customers?** Identified top-tier customers by total asset balance for private banking targeting.
2. **Which customers pose the highest loan risk?** Flagged "Defaulted" accounts with high outstanding balances.
3. **What are the transaction patterns of high-value customers?** Analyzed liquidity movement and volatility in debit vs. credit behavior.
4. **How can we optimize query performance for scale?** Implemented strategic B-Tree indexing and materialized views.
5. **What fraud-like patterns exist in transaction data?** Utilized statistical outlier detection to identify suspicious transactions.

## 💡 Key Findings & Insights
* **Revenue Leaders**: Mary ($924,772), Linda ($905,899), and Christopher ($750,876) are the bank's top asset holders.
* **Risk Mitigation**: Richard ($316,918) was identified as the highest default risk, requiring immediate collection intervention.
* **Transaction Patterns**: High-value customers utilize Debit transactions more frequently (3,201) than Credit (2,186).
* **Fraud Detection**: Flagged 3,145 anomalous transactions that exceeded 3 standard deviations from the mean amount.

## 🛠️ Technical Implementation
* **Data Quality Layer**: Built a validation suite to detect NULL balances, orphaned accounts, and duplicate records.
* **Advanced Analytics**: Leveraged **Window Functions** (`RANK`, `LAG`) to calculate asset rankings and daily spending volatility.
* **Optimization**: Created indexes on foreign keys (`customer_id`, `account_id`) to ensure sub-second JOIN performance.
* **Automation**: Developed a **Materialized View** (`mv_customer_360`) to provide a pre-aggregated view of customer health for BI dashboards.

## 🎯 Conclusion
This analysis identifies a strong asset base but highlights significant threats from high-value defaults. By transitioning to automated risk triggers and technical optimizations, the bank can protect liquidity and improve its overall risk posture.
