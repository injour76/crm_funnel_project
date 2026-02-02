CRM Funnel & Retention Analysis (Lifecycle & Contract-Based Churn)

Objective 

Analyze customer churn across lifecycle stages to identify high-risk segments and propose targeted CRM intervention opportunities that improve retention. 

 

Dataset 

Telco Customer Churn Dataset (IBM) 
Includes customer tenure, contract type, billing information, and churn indicators. 

Key fields used: 

tenure_months 

contract 

monthly_charges 

churn_label 

 

Lifecycle Definition 

Customers were segmented into lifecycle stages based on tenure: 

Onboarding: 0–3 months 

Early Lifecycle: 4–12 months 

Established: 13+ months 

This mirrors how CRM teams monitor customer health over time. 

 

Key Metrics 

Churn rate by lifecycle stage 

Churn rate by lifecycle stage × contract type 

Churn rate is calculated as the percentage of customers labeled as churned (churn_label = "Yes"). 

 

Key Insights 

Onboarding customers on month-to-month contracts show the highest churn (~58%), making this the most critical risk segment. 

During onboarding, month-to-month churn is ~6× higher than one-year contracts and significantly higher than two-year contracts (near 0%). 

Churn stabilizes for long-term contracts as tenure increases, but established month-to-month customers still churn at a high rate (~34%), indicating ongoing risk. 

 

CRM Recommendations 

1. Early Onboarding Intervention 

Target: Onboarding customers on month-to-month contracts 

Action: Trigger a multi-touch onboarding journey (email/SMS) within the first 14 days, including feature education and support prompts 

KPI: 30-day retention rate 

 

2. Contract Conversion Campaign 

Target: Month-to-month customers within the first 30 days 

Action: A/B test a limited-time incentive to convert users to one-year contracts 

KPI: Contract conversion rate and churn reduction 

 

3. Retention for Established Month-to-Month Users 

Target: Established customers still on month-to-month plans 

Action: Enroll users in a loyalty or renewal campaign emphasizing long-term value 

KPI: 90-day retention rate 

 

Tools Used 

SQL (SQLite) for metric aggregation and segmentation validation

Python (Pandas) for data cleaning, lifecycle segmentation, and churn calculations 

Jupyter Notebook for analysis and reproducibility 

 

 

Assumptions & Limitations 

Lifecycle stages were inferred from tenure due to lack of event-level activation data 

Churn analysis is based on historical labels and does not imply causal relationships 

Results reflect segment-level trends and should be validated through controlled experiments (A/B tests) 

Dataset represents a snapshot in time and may not capture seasonality or recent behavior changes 

 

Summary 

This analysis identifies early lifecycle and contract structure as primary drivers of churn and outlines specific, testable CRM actions tied to retention KPIs. The approach reflects how CRM analytics teams diagnose churn and prioritize interventions in production environments. 

 