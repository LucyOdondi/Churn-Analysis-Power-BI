This project analyzes customer churn behavior in a betting platform using Power BI and Excel. The dashboard explores churn through various variances and churn risk factors to identify which customers are most likely to leave and what retention strategies could reduce revenue loss. 

The analysis combines DAX calculations, behavioral analytics, and revenue impact modeling to identify the strongest predictors of churn and support retention decision-making.

 The top cards display the datasets main identifiers such as the total customers, churn rate and churned customers. The tables below shows graphs and charts on how different variances contributed to churning. 

**Business Problem**

Identify why and where customer churn was causing revenue loss on a betting platform.  

**Business Objective**

The goal of this dashboard is to analyze betting activity and identify patterns that can help improve:

- Customer engagement and retention strategies
- Revenue tracking
- Betting performance monitoring
- Risk analysis
- Decision-making through data visualization

## Key Findings

- Customers inactive for 30+ days showed highest churn risk.
- Low-frequency bettors churned significantly more than active bettors.
- Frequent support interactions correlated with increased churn.
- Revenue at risk exceeded $100K.

## Recommendation

- Target inactive users with retention campaigns.
- Introduce VIP engagement programs.
- Trigger reactivation offers after 14 days of inactivity.

**Dax Measures**

**Active Customers** (30 Days) = CALCULATE(COUNT(betting_customer_churn_mock_data[CustomerID]),betting_customer_churn_mock_data[LastLoginDaysAgo] >=30
)

**Churn Rate** = DIVIDE(betting_customer_churn_mock_data[Churned Customers],betting_customer_churn_mock_data[Total Customers])

**Churned Customers** = CALCULATE(COUNT(betting_customer_churn_mock_data[Churn]),betting_customer_churn_mock_data[Churn]="Yes")

**Total Customers** = COUNT(betting_customer_churn_mock_data[CustomerID])

**Total Deposits** = SUM(betting_customer_churn_mock_data[MonthlyDepositUSD])

**Tools Used**

- Power BI Desktop
- Power Query
- DAX (Data Analysis Expressions)
- Excel / CSV datasets
