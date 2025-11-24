# KARIM PROMOTION AI

A machine learning project to predict employee promotion eligibility using performance metrics, training data, and work arrangement features.

## 🎯 Overview

This project implements a binary classification model to predict employee promotions based on:
- **Performance metrics** (KPIs, ratings, awards)
- **Training & development** (courses, scores)
- **Work arrangement** (full-time, part-time, shifts)
- **Demographics** (age, tenure, education)

### Key Features:
✅ Handles severe class imbalance (typical 5-15% promotion rate)  
✅ Comprehensive fairness analysis  
✅ Production-ready prediction API  
✅ Ethical AI (no discriminatory features)  

## 🚀 Quick Start

### Run notebooks in order

- 1-data-preprocessing.ipynb   
- 2-data-analysis.ipynb        
- 3-feature-engineering.ipynb  
- 4-model-selection.ipynb
- 5-training-evaluation.ipynb
- 6-testing-model.ipynb

for example: 
```bash
jupyter notebook notebooks/1-data-preprocessing.ipynb
```

1. Open the notebook in your browser
2. Click **Cell > Run All**


## 📊 Dataset Information

### Required Columns

Your CSV file (`data/employee_dataset.csv`) must contain these columns:

| Column | Type | Description | Valid Values |
|--------|------|-------------|--------------|
| age | int | Employee age | 18-100 |
| gender | string | Gender | M, F |
| department | string | Department name | Any string |
| education | string | Education level | High School, Bachelor's, Master's, PhD |
| tenure_years | float | Years with company | 0-50 |
| previous_rating | int | Performance rating | 1-5 |
| kpi_met | int | KPI achievement % | 0-100 |
| trainings_attended | int | # of trainings | 0+ |
| avg_training_score | float | Avg training score | 0-100 |
| awards_won | int | # of awards | 0+ |
| job_level | int | Job level | 1-5 |
| region | string | Geographic region | Any string |
| recruitment_channel | string | How hired | Direct, Referral, Agency |
| work_type | string | Work arrangement | Full-Time, Part-Time Day, Part-Time Night |
| language_count | int | # of languages | 1, 2, 3+ |
| multilingual | int | Speaks multiple languages | 0, 1 |
| international_hire | int | Hired internationally | 0, 1 |
| is_promoted | int | Target variable | 0 (no), 1 (yes) |

---

## 🤖 Model Details

### Implemented Algorithms

1. **Logistic Regression** (Interpretable Baseline)
   - Highly interpretable coefficients
   - Good for explaining to HR
   - Fast inference

### Evaluation Metrics

Focus on these metrics (NOT accuracy due to class imbalance):

- **F1 Score**: Harmonic mean of precision and recall
- **PR-AUC**: Area under Precision-Recall curve (best for imbalanced data)
- **ROC-AUC**: Overall discrimination ability
- **Precision**: Of predicted promotions, how many are correct
- **Recall**: Of actual promotions, how many we catch

---

**⚠️ Important Disclaimer**: This model is designed to **assist** HR decision-making, not replace it. Always include human review in promotion decisions to ensure fairness, consider context the model cannot capture, and comply with employment laws in your jurisdiction.