Employee Attrition & Performance
Analytics
GlobalTech Solutions | HR Analytics | Classification | People Analytics
April 2025
1. Executive Summary
GlobalTech Solutions is experiencing a 30% employee attrition rate — double the industry average of
15% — resulting in significant talent loss and rising hiring costs. This project builds a classification
model using Logistic Regression and Random Forest to predict which employees are likely to leave.
245 high-risk employees were identified and a priority HR action list was generated. The model
achieved a ROC-AUC of 0.722.
2. Problem Definition
Business Problem
• 30% annual attrition rate — double the industry average of ~15%
• Loss of skilled employees causing productivity decline across teams
• Rising recruitment and training costs due to frequent backfills
• No early warning system to identify at-risk employees before they resign
• HR team relies on exit interviews — reactive, not proactive
Key Objectives
• Build a model to predict which employees are likely to leave
• Identify the top factors driving attrition across the organisation
• Analyse the relationship between performance, satisfaction, and attrition
• Segment all 1,000 employees into High / Medium / Low attrition risk
• Provide HR with a prioritised action list for immediate intervention
• Recommend targeted retention strategies per risk segment
3. Dataset Description
Dataset Attribute Details
Total Employees 1,000
Total Features 18 (16 input + 1 ID + 1 target)
Key Features Monthly Income, Overtime Hours, Job
Satisfaction, Years at Company, Absenteeism
Target Variable Attrition (No = Stayed, Yes = Left)Class Distribution 700 Stayed (70%) | 300 Left (30%)
Missing Values None — dataset fully clean
Departments IT, Sales, HR, Finance, Operations, Support
4. Methodology & Data Preprocessing
Data Preprocessing
• Label Encoding applied to all text columns: Gender, Department, Role, Education, Attrition
• Dropped EmployeeID — not a predictive feature
• Train/Test split: 80/20 with stratified sampling to maintain 30% attrition ratio in both sets
• StandardScaler applied to normalise all numeric features
Modelling Approach
• Model 1 — Logistic Regression: interpretable baseline with probability output
• Model 2 — Random Forest (100 trees): stronger ensemble model
• Evaluation: Accuracy, Precision, Recall, F1 Score, ROC-AUC, Confusion Matrix
• Feature importance from Random Forest used to rank attrition drivers
• All 1,000 employees scored with attrition probability (0–100%)
• Three-tier risk segmentation: Low (<35%), Medium (35–60%), High (>60%)
5. Results & Model Performance
KPI / Metric Target / Benchmark
Logistic Regression — Accuracy 74.5%
Logistic Regression — ROC-AUC 0.714
Random Forest — Accuracy 75.0%
Random Forest — ROC-AUC 0.722
Top 3 Attrition Drivers Monthly Income, Overtime Hours, Years at
Company
Highest Risk Department Sales (35.9% attrition rate)
High Risk Employees Flagged 245 out of 1,000 (24.5%)
Risk Segmentation
Risk Tier Action
High Risk (>60% prob) 245 employees — immediate HR intervention
required
Medium Risk (35–60%) 74 employees — monitor and engageproactively
Low Risk (<35%) 681 employees — standard engagement
programme
6. Business Recommendations
• Conduct retention interviews with all 245 HIGH RISK employees this quarter
• Introduce overtime cap at 20 hours/month — overtime is the 2nd strongest attrition driver
• Expand remote work flexibility — linked to higher job satisfaction scores
• Create structured promotion track — PromotionLast5Years scored very low across leavers
• Increase training budget — low training hours strongly correlated with exit
• Focus immediate HR resources on the Sales department (highest attrition at 35.9%)
• Introduce stay bonuses for employees at the 2–3 year tenure mark (highest risk window)
• Run this model monthly on fresh HR data — alert when any employee crosses 60% threshold
7. Conclusion & Future Work
• Random Forest (ROC-AUC 0.722) outperforms Logistic Regression for attrition prediction
• Monthly Income, Overtime, and Tenure are the three dominant attrition drivers
• 245 employees are currently at high risk — immediate intervention can prevent costly exits
• Future work: XGBoost model, real-time HR dashboard, NLP on exit interview feedback
• Target: reduce attrition from 30% to below 20% within 12 months of intervention
