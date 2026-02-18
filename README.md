Healthcare Readmission Analytics & Diabetes Risk Prediction
📌 Project Overview

This project analyzes hospital readmission patterns of diabetes patients and builds a predictive model to identify high-risk patients. It combines data analysis, machine learning, and interactive Power BI dashboards to provide actionable healthcare insights.
The goal is to help hospitals reduce readmissions, improve patient care, and optimize medical resources.

📊 Dataset Information

Source: UCI Machine Learning Repository
Dataset Name: Diabetes 130-US Hospitals (1999–2008)
Time Period: 1999 to 2008
Records: 100,000+ patient encounters
Hospitals: 130+ hospitals in the USA

Files Used:

diabetic_data.csv – Main patient dataset
IDS_mapping.csv – Mapping file for diagnosis codes

🛠️ Tools & Technologies

Python (Google Colab)
Pandas, NumPy
Matplotlib, Seaborn
Scikit-learn
Power BI Desktop
Data modeling
DAX measures
Interactive dashboards
GitHub


🔍 Project Workflow
Phase 1: Data Collection

Downloaded dataset from UCI Repository
Extracted compressed files
Loaded data into Google Colab

Phase 2: Data Cleaning & Preprocessing

Performed multiple cleaning steps:
Replaced missing values (?) with NaN
Handled missing columns using appropriate strategies
Removed unnecessary ID columns
Converted categorical variables using one-hot encoding
Standardized numerical features
Removed inconsistent records
Created new calculated columns
Example:
Converted readmitted column to binary target
Created risk_prediction column from ML output

Phase 3: Exploratory Data Analysis (EDA)

Conducted detailed EDA to understand data patterns:
Missing value analysis
Distribution analysis
Correlation analysis
Outlier detection
Feature relationships

Visualizations:

Histograms
Bar charts
Heatmaps
Box plots

Key Insights:

Elderly patients have higher readmission rates
Higher medication count increases risk
Longer hospital stays correlate with readmission
Emergency visits indicate higher risk

🤖 Phase 4: Machine Learning Model
Model Used:

Logistic Regression

Objective:

Predict whether a patient will be readmitted (High Risk / Low Risk)
First Model (Baseline)
Used default Logistic Regression
Trained on encoded data
Evaluated using accuracy and classification report

Result:

High accuracy but poor minority class recall
Imbalanced data issue observed
Improved Model (Optimized)
Second model was built for better performance:
Improvements:
Feature scaling
class_weight = balanced
Solver optimization
Increased iterations
LogisticRegression(
    max_iter=300,
    solver='liblinear',
    class_weight='balanced'
)


Result:

Better recall for high-risk patients
Improved model stability
Reduced bias

Final Output

Generated predictions for all patients
Added risk_prediction column
Exported clean dataset for Power BI

📈 Phase 5: Power BI Dashboards

Three interactive dashboards were created.

📄 1️⃣ Readmission Analytics Dashboard (Overview Page)

Purpose:
Provide high-level hospital performance overview.

KPIs:
Total Patients
Readmission Rate
High-Risk Patients
Average Length of Stay
Visuals:
Readmission status distribution
Age vs readmission
Gender distribution
Summary charts

Business Insight:
Helps management understand overall hospital readmission trends.

📄 2️⃣ Risk Behaviour Analysis Dashboard

Purpose:
Analyze behavioral and clinical patterns that influence risk.
Visuals:
Medication count vs risk
Emergency visits vs risk
Length of stay vs risk
Inpatient visits vs risk

Filters:
Age group
Gender
Race
Medical specialty

Features:
Interactive slicers
Professional layout
Clear section headers

Business Insight:
Identifies patient behavior patterns leading to higher risk.

📄 3️⃣ High-Risk Patient Monitoring Dashboard

Purpose:
Monitor individual high-risk patients.

Table Includes:
Age
Gender
Race
Specialty
Stay duration
Medications
Emergency visits
Inpatient visits

Advanced Features:
Conditional formatting
Risk color coding
Highlighted critical cases

Color Rules:
Green: Low risk
Yellow: Medium risk
Red: High risk

Business Insight:
Supports doctors and hospital staff in early intervention.

🎯 Key Findings

Patients with >20 medications show high readmission risk
Longer stays (>10 days) increase probability
Multiple inpatient visits indicate chronic risk
Emergency visits strongly correlate with readmission
Elderly patients form highest-risk segment

🚀 Business Impact

This project helps hospitals:

✔ Reduce readmission penalties
✔ Improve patient outcomes
✔ Optimize staff allocation
✔ Identify high-risk patients early
✔ Support data-driven healthcare decisions

📁 Repository Structure
Healthcare-Analysis/
│
├── healthcare Analysis/        # Python notebooks & data
├── Healthcare Analysis Dashboard.pbix
├── Dashboard Screenshots/
├── final_data_clean.csv
└── README.md

👤 Author

Siddarth Sharma
Aspiring Data Analyst / Data Scientist
Focused on Healthcare Analytics & Business Intelligence
