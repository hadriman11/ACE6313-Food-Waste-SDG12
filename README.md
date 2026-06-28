# ACE6313-Food-Waste-SDG12

Machine learning analysis of global food waste data, supporting **UN Sustainable Development Goal 12: Responsible Consumption and Production**.

## Project Overview

This project applies machine learning to the UNEP Food Waste Index dataset (214 countries) to predict the **confidence level** of national food-waste estimates from waste figures and regional data. The work covers a full pipeline: data preprocessing, model training, hyperparameter tuning, and evaluation.

## Team

| Member | Role | Student ID |
|--------|------|------------|
| *Name 1* | Data Preprocessing (Part A) | *ID* |
| *Name 2* | Machine Learning Models (Part B) | *ID* |

## Dataset

- **Source:** [UNEP Food Waste Index Report](https://www.unep.org/resources/report/unep-food-waste-index-report) (via Kaggle)
- **Rows:** 214 countries
- **Target:** `Confidence in estimate` (Very Low / Low / Medium / High)
- **Features:** household, retail, and food-service waste (kg/capita/year and tonnes/year), region

## Repository Structure

```
ACE6313-Food-Waste-SDG12/
├── README.md                       # this file
├── PROPOSAL.md                     # interim proposal & dataset description
├── data/
│   ├── food_waste.csv              # raw dataset
│   └── clean_food_waste.csv        # output of Part A (created by notebook)
├── notebooks/
│   ├── Part_A_Preprocessing.ipynb  # Student 1
│   └── Part_B_ML_Models.ipynb      # Student 2
├── report/                         # figures + final report
└── scripts/                        # optional .py versions
```

## How to Run

1. Install [Anaconda](https://www.anaconda.com/download) (includes Python, Jupyter, scikit-learn).
2. Clone this repo:
   ```bash
   git clone https://github.com/hadriman11/ACE6313-Food-Waste-SDG12.git
   cd ACE6313-Food-Waste-SDG12
   ```
3. Launch Jupyter:
   ```bash
   jupyter notebook
   ```
4. Run `notebooks/Part_A_Preprocessing.ipynb` first (creates `clean_food_waste.csv`).
5. Then run `notebooks/Part_B_ML_Models.ipynb`.

## Methods

**Part A — Preprocessing:** missing-value/duplicate checks, outlier detection (IQR), label encoding, feature engineering (sector ratios), StandardScaler, correlation analysis, and PCA.

**Part B — Modelling:** six algorithms (Logistic Regression, Decision Tree, Random Forest, SVM, kNN, Gradient Boosting), hyperparameter tuning via GridSearchCV, evaluated with accuracy, precision, recall, and weighted F1-score.

## Requirements

Python 3.x with: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn` (all included in Anaconda).
