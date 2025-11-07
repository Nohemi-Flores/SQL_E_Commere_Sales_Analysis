# SQL - Sales Analysis

## Overview
Analysis of customer behavior, retention, and lifetime value for an e-commerce company to improve customer retention and maximize revenue.

## Business Questions
1. **Customer Segmentation**: Who are our most valuable customers?

2. **Cohort Analysis**: How do different customer groups generate revenue?

3. **Retention Analysis** Which customers have not purchased recently?

## Analysis Approach

## 1. Customer Segmentation Analysis
- Customers categorized based on total lifetime value (LTV)
- Customers assigned to High, Mid, and Low-value segments
- Key metrics calculated: total revenue

💻 Query: [1_customer_segmentation.sql](/1_customer_segmentation.sql)

**📈 Visualization**

![Customer Segmentation Analysis](/images/1_Customer_Segmentation.png)

📊 **Key Findings**
- High-value segment (25% of customers) drives 66% of revenue ($135.4M)
- Mid-value segment (50% of customers) generates 32% of revenue ($66.6M)
- Low-value segment (25% of customers) accounts for 2% of revenue ($4.3M)

💡 **Business Insights**:
- **High-value (66% revenue)**: Offer a premium membership program to 13,372 VIP customers. Losing one customer significantly impacts revenue.
- **Mid-value (32% revenue)**: Create upgrade paths through personalized promotions, with potential $66.6M ⇾ $135.4M revenue opportunity
- **Low-value (2% revenue)**: Design re-engagement campaigns and price-sensitive promotions to increase purchase frequency

### 2. Cohort Analysis
- Tracked revenue and customer count per cohorts
- Cohorts were grouped by year of first purchase
- Analyzed customer retention at a cohort level

💻 Query: [2_cohort_analysis.sql](/2_cohort_analysis.sql)

**📈 Visualization**

![Cohort Analysis](/images/2_bar_chart.png)

📊 **Key Findings**
- Revenue per customer shows an alarming decreasing trend over time
    - 2022-2024 cohorts consistently perform worse than earlier cohorts
    - NOTE: While net revenue might be increasing, this is likely due to a larger customer base. It does not necessarily show an increase in customer value.

💡 **Business Insights**:
- Individual customer value is decreasing over time, which needs further investigation.
- 2023 saw a drop in number of customers acquired. This is concerning.
- The last two points show that the company is facing a potential revenue decline.

### 3. Customer Retention
- Identified customers at risk of churning
- Last purchase patterns analyzed
- Customer-specific metrics calculated

💻 Query: [3_retention_analysis.sql](/3_retention_analysis.sql)

**📈 Visualization**

![retention analysis](/images/3_bar_chart.png)

📊 **Key Findings**
- Cohort churn stabilizes at ~90% after 2-3 years, which indicates a predictable long-term retention pattern.
- Retention rates are consistently low (8-10%) across all cohorts, suggesting retention issues are systematuc rather than specific to certain years.
- Newer cohorts (2022-2023) show similar churn trajectories, which signals that without intervention, future cohorts will follow the same pattern.

💡 **Business Insights**:
- Strengthen early engagement strategies to target the first 1-2 years with onboarding incentives, loyalty rewards, and personalized offers to improve long-term retention.
- By focusing on targeted win-back campaigns rather than broad retention efforts, high-value churned customers will be re-engaged, which may yield higher ROI.
- Predict & preempt churn risk and use customer-specific warning indicators to proactively intervene wit at-risk users before they lapse.

## Strategic Recommendations

1. **Customer Value Optimization (Customer Segmentation)**
    
    -  **High-Value Segment Loyalty Program**: 
Introduce a VIP membership with exclusive perks (priority service, early access, personalized rewards) to retain the 25% of customers driving 66% of revenue.

    - **Mid-Value Segment Upsell Strategy**:
Launch targeted promotions and upgrade incentives to encourage mid-value customers to increase spend and transition into the high-value tier.

2. **Cohort Performance Strategy (Customer Revenue by Cohort)**
    - **Acquisition Quality Audit**:
Investigate changes in marketing channels, onboarding, and product experience for 2022–2024 cohorts to identify why customer value is declining.

    - **High-LTV Targeting**:
Refocus acquisition efforts on high-potential customer profiles using predictive modeling and segmentation to improve future cohort performance.

3. **Retention & Churn Prevention (Customer Retention)**
    - **Early Lifecycle Engagement**: 
Implement onboarding campaigns with personalized offers and loyalty rewards to boost retention during the critical first 1–2 years.

    - **Predictive Churn Prevention**:
Use customer-specific churn indicators to proactively trigger win-back campaigns and personalized outreach before customers lapse.

## Technical Details
- **Database**: PostgreSQL
- **Analysis Tools**: PostgreSQL, PGadmin
- **Visualization**: Copilot
