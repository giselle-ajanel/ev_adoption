# Predicting U.S. Electric Vehicle Adoption Across Socioeconomic Indicators

A data science and econometric modeling framework designed to analyze and predict Electric Vehicle (EV) adoption rates across U.S. states using longitudinal socioeconomic and infrastructure data. Built to quantify regional adoption barriers and evaluate market expansion dynamics for policymakers and industry stakeholders.


## Overview

Accelerating the transition to electric mobility requires understanding how underlying socioeconomic factors drive regional adoption rates. This project analyzes 400 state-year observations spanning from 2016 through 2023, leveraging data from the National Renewable Energy Laboratory (NREL), U.S. Census Bureau, and Energy Information Administration (EIA).

By executing dimensionality reduction and regression modeling (Multiple Linear Regression & Random Forest Regression), the system identifies key economic drivers—such as per capita income, educational attainment, and labor force participation—that influence EV market penetration.



## Key Technical Highlights

* **Data Engineering & Compression:** Aggregated multi-source national datasets and compressed 36 initial variables down to 6 core indicators to eliminate multicollinearity while preserving explanatory variance.
* **Econometric & Statistical Modeling:** Built and evaluated Multiple Linear Regression and Random Forest Regressor models using Python to forecast state-level adoption trends.
* **Key Findings:** Identified **per capita income** as the primary driver of regional EV adoption, exhibiting approximately 14 times higher predictive weight compared to secondary indicators like bachelor degree attainment and labor force participation.

---

## Repo Structure

* `data/` — Raw and processed state-level datasets (NREL, Census Bureau, EIA)
* `notebooks/` — Jupyter notebooks containing exploratory data analysis, variable reduction, and model training
* `src/` — Python scripts for data preprocessing pipeline, feature engineering, and evaluation metrics
* `visualizations/` — Output charts showing variable importance, correlation matrices, and regional adoption maps

---

## System Workflow

1. **Data Ingestion & Cleaning:**
   * Consolidated longitudinal data from NREL (charging infrastructure), U.S. Census Bureau (demographics/income), and EIA (energy metrics).
   * Handled missing values, standardized unit variance across state-year observations, and computed scaled adoption rates.

2. **Feature Reduction & Selection:**
   * Analyzed correlation structures to reduce redundancy across 36 socioeconomic metrics.
   * Selected 6 non-redundant indicators balancing predictive power and model interpretability.

3. **Model Training & Evaluation:**
   * Trained Multiple Linear Regression baselines alongside Random Forest Regressor models.
   * Evaluated feature importance metrics to rank key drivers of consumer adoption.

---

## Tech Stack

* **Python 3.8+**
* **Data Processing & Analysis:** `pandas`, `numpy`, `scipy`
* **Machine Learning & Modeling:** `scikit-learn`, `statsmodels`
* **Visualization:** `matplotlib`, `seaborn`

