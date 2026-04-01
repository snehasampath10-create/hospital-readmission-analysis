# hospital-readmission-analysis
Healthcare analytics project analyzing hospital readmission patterns

## 📊 Project Overview
Analysis of hospital readmission patterns for diabetic patients using real-world data from 130 US hospitals (1999-2008). This project identifies key risk factors that predict 30-day hospital readmissions.

## 🎯 Objective
Identify patients at high risk of readmission within 30 days to enable targeted interventions and improve patient outcomes.

## 📁 Dataset
- **Source:** UCI Machine Learning Repository - Diabetes 130-US Hospitals
- **Size:** 100,000+ patient records
- **Features:** 50+ variables including demographics, diagnoses, medications, and procedures
- **Target:** Readmission within 30 days (<30)

## 🔍 Key Findings

### Readmission Rate
- **11.2%** of patients are readmitted within 30 days
- Highly imbalanced dataset

### Strong Predictors Identified

1. **Age (50-80 years)**
   - Older patients show higher readmission rates
   - Peak risk in 70-80 age group

2. **Number of Medications**
   - Readmitted patients: 15 medications (median)
   - Non-readmitted patients: 13 medications (median)
   - Higher medication complexity = higher risk

3. **Prior Emergency Visits**
   - Patients with history of frequent ER visits have higher readmission risk
   - "Frequent flyers" are a high-risk group

4. **Prior Inpatient Visits**
   - Previous hospitalizations predict future readmissions
   - Indicates chronic health conditions
     
## 🤖 Predictive Modeling Results

### Model Performance
- **Algorithm:** Random Forest Classifier
- **ROC-AUC Score:** 0.67 (industry standard for readmission prediction)
- **Accuracy:** 70.86%
- **Recall:** 50% (catches half of readmitted patients)

### Top Predictive Features
1. Prior inpatient visits (most important)
2. Total hospital encounters
3. Discharge disposition
4. Number of medications
5. Prior emergency visits
6. Patient age

### Model Validation
- Train/test split: 80/20
- Handles class imbalance with balanced weights
- Performance validated on 20,354 unseen patients

## 💡 Recommendations

### High-Risk Patient Profile
Target interventions for:
- Age 50-80 years
- 15+ medications
- History of frequent ER/hospital visits

### Suggested Interventions
- Medication review before discharge
- Follow-up calls within 7 days
- Care coordination for frequent users
- Enhanced patient education on medication management

## 🛠️ Tools & Technologies
- **Python** (pandas, numpy, matplotlib, seaborn)
- **Jupyter Notebook** (Google Colab)
- **Statistical Analysis** & Data Visualization

## 📂 Repository Structure
```
hospital-readmission-analysis/
├── data/
│   ├── raw/                           # Original dataset
│   │   └── diabetic_data.csv
│   └── processed/                     # Cleaned and engineered data
│       ├── diabetic_data_cleaned.csv
│       └── diabetic_data_model_ready.csv
├── notebooks/
│   ├── 01_data_exploration.ipynb      # Initial EDA and insights
│   ├── 02_data_cleaning.ipynb         # Data cleaning pipeline
│   ├── 03_feature_engineering.ipynb   # Feature creation and encoding
│   └── 04_modeling.ipynb              # Model building and evaluation
├── outputs/                           # Visualizations and charts
└── README.md
```


## 👤 Author
**Sneha**
- Data Analyst with 5+ years of experience
- Background in software engineering and statistical analysis

---
*This project demonstrates end-to-end data analysis skills including exploratory data analysis, statistical reasoning, data visualization, and deriving actionable business insights.*
