# Student Depression Risk Prediction Using Machine Learning

## Project Overview

Mental health challenges among university students have become an increasing global concern. Many students experiencing depression remain unidentified until symptoms become severe, limiting opportunities for early intervention and support.

This project leverages **Machine Learning**, **Statistical Analysis**, and **Exploratory Data Analysis (EDA)** to identify the major factors associated with student depression and build predictive models capable of estimating an individual's depression risk.

Using **27,901 student records** containing demographic, academic, financial, lifestyle, and mental health information, two supervised learning algorithms—**Logistic Regression** and **Random Forest**—were developed and compared to determine the most effective predictive model.

To demonstrate a practical application, the project also includes an interactive depression risk assessment system that estimates a student's probability of depression and classifies the result into interpretable risk categories suitable for early screening.

---

# Analysis Problem

Universities typically depend on students voluntarily seeking psychological support after symptoms have progressed. Unfortunately, many students delay asking for help due to stigma, lack of awareness, or limited access to mental health resources.

The challenge is to determine whether historical student information can be used to identify individuals who may be at elevated risk before their condition worsens.

This project answers three key questions:

- Which student characteristics are most strongly associated with depression?
- Which machine learning algorithm provides the most accurate predictions?
- How can predictive analytics be transformed into an interpretable decision-support tool for early intervention?

---

# Project Objectives

The project aims to:

- Clean and preprocess real-world survey data
- Explore relationships between demographic, academic, financial, and lifestyle variables
- Identify statistically significant predictors of depression
- Train and evaluate multiple classification algorithms
- Compare model performance using industry-standard evaluation metrics
- Build an interactive depression risk prediction system
- Generate actionable insights that support proactive student wellbeing initiatives

---

# Dataset Source

### Student Depression Dataset [Here](https://www.kaggle.com/datasets/hopesb/student-depression-dataset)

### Dataset Summary

| Attribute | Value |
|-----------|------:|
| Records | 27,901 |
| Features | 21 |
| Target Variable | Depression |
| Problem Type | Binary Classification |
| Missing Values | Financial Stress |
| Duplicate Records | None |

### Target Distribution

| Class | Count | Percentage |
|--------|------:|-----------:|
| Depressed | 16,336 | 58.5% |
| Not Depressed | 11,565 | 41.5% |

The dataset captures multiple dimensions of student life, including demographics, academics, finances, lifestyle behaviours, and mental health history.

---

# Features

## Demographic

- Gender
- Age
- City
- Degree
- Profession

## Academic

- Academic Pressure
- Study Satisfaction
- CGPA

## Lifestyle

- Sleep Duration
- Dietary Habits
- Work/Study Hours

## Financial

- Financial Stress

## Mental Health

- Family History of Mental Illness
- Suicidal Thoughts

---

# Technology Stack

- Python
- Jupyter Notebook
- Pandas
- NumPy
- SciPy
- Matplotlib
- Seaborn
- Scikit-learn

---

# Project Workflow

## 1. Data Preprocessing

The dataset underwent comprehensive preprocessing to ensure data quality before modelling.

### Data Cleaning

- Missing value imputation using median values
- Duplicate verification
- Data type correction
- Label encoding
- Ordinal encoding
- Feature transformation
- Data validation

---

## 2. Exploratory Data Analysis (EDA)

Exploratory analysis was conducted to understand distributions, relationships, and potential predictors of depression.

### Visualizations

- Distribution plots
- Count plots
- Histograms
- Boxplots
- Correlation heatmaps
- Crosstab analysis
- Bar charts

The EDA stage helped uncover trends, detect anomalies, and guide feature selection for modelling.

---

## 3. Statistical Analysis

To quantify relationships identified during EDA, statistical tests were applied.

### Point-Biserial Correlation

Measured associations between continuous variables and the binary depression outcome.

### Cramér's V

Measured the strength of association between categorical variables and depression.

These analyses identified the variables with the strongest predictive potential before model development.

---

# Machine Learning Pipeline

## Data Split

- Training Set: 80%
- Testing Set: 20%
- Stratified Sampling
- Random State = 42

## Feature Scaling

Numerical variables were standardized using **StandardScaler** before training the Logistic Regression model to prevent data leakage and improve model performance.

---

# Models Developed

## Logistic Regression

A linear probabilistic classifier that estimates the likelihood of depression.

### Advantages

- High interpretability
- Fast training
- Probability estimates
- Explainable coefficients

---

## Random Forest

An ensemble learning algorithm consisting of **300 decision trees** trained using bootstrap aggregation.

### Advantages

- Captures nonlinear relationships
- Automatically models feature interactions
- Resistant to overfitting
- Provides feature importance rankings

---

# Model Evaluation

Models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
- Confusion Matrix

---

# Performance Comparison

| Metric | Logistic Regression | Random Forest |
|---------|-------------------:|--------------:|
| Accuracy | **79.6%** | 77.9% |
| Precision | **81.0%** | 80.5% |
| Recall | **85.2%** | 82.0% |
| F1 Score | **83.0%** | 81.3% |
| ROC-AUC | **86.6%** | 84.7% |

---

# Model Selection

Although Random Forest successfully captured nonlinear relationships, **Logistic Regression** consistently achieved superior performance across every evaluation metric while offering greater interpretability. Its probability outputs also make it well suited for practical mental health screening, leading to its selection as the final deployment model.

---

# Interactive Depression Risk Prediction System

The final Logistic Regression model was integrated into a command-line application capable of:

- Predicting an individual's probability of depression
- Assigning an interpretable risk category
- Generating unique Student IDs
- Storing assessment history
- Exporting prediction results to CSV
- Retrieving previous assessments

## Risk Categories

| Probability | Risk Level |
|-------------|------------|
| <30% | Low |
| 30–59% | Moderate |
| 60–79% | High |
| ≥80% | Critical |

---

# Key Insights

## 1. Academic Pressure Emerged as the Strongest Predictor

Academic pressure exhibited the strongest positive association with depression (**r = 0.47**). Depression prevalence increased from **44%** among students reporting the lowest pressure to **86%** among those reporting the highest pressure.

---

## 2. Financial Stress Was a Major Risk Factor

Students experiencing the highest levels of financial stress recorded an **81.3%** depression rate, compared with **31.9%** among those reporting minimal financial stress.

---

## 3. Younger Students Were More Vulnerable

Students aged **18–20 years** experienced the highest depression prevalence (**72.3%**), with rates steadily decreasing across older age groups.

---

## 4. Healthy Lifestyle Habits Reduced Risk

| Lifestyle Factor | Depression Rate |
|------------------|----------------:|
| Healthy Diet | 45.4% |
| Unhealthy Diet | 70.7% |
| ≥8 Hours Sleep | 50.9% |
| <5 Hours Sleep | 64.5% |

These findings suggest that healthier lifestyle behaviours are associated with lower depression prevalence.

---

## 5. Depression Strongly Coincided with Suicidal Thoughts

Among students classified as depressed, **85.4%** also reported suicidal thoughts, highlighting the importance of integrated mental health screening and timely professional support.

---

## 6. Multiple Risk Factors Amplified Depression Risk

Students simultaneously experiencing:

- High academic pressure
- High financial stress
- Poor sleep
- Unhealthy dietary habits

recorded an observed depression rate of **97.6%**, compared with **1.1%** among students with consistently low-risk profiles.

This finding demonstrates that combining multiple indicators substantially improves risk assessment compared with evaluating individual factors in isolation.

---

# Recommendations

Based on the findings, educational institutions should consider:

- Expanding academic support services and workload management programmes
- Increasing financial aid and emergency assistance initiatives
- Improving access to on-campus mental health professionals
- Implementing confidential routine mental health screening
- Promoting healthy sleep, nutrition, and wellbeing campaigns
- Leveraging predictive analytics to proactively identify students who may benefit from early intervention

---

# Conclusion

This project demonstrates how **Data Analytics**, **Statistical Inference**, and **Machine Learning** can be combined to address an important public health challenge.

Beyond achieving strong predictive performance, the project translates model outputs into a practical decision-support tool capable of identifying students who may require early mental health intervention.

By combining interpretability with robust classification performance, the final **Logistic Regression** model provides a foundation for scalable, data-informed student wellbeing initiatives.
