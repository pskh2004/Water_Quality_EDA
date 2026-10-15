# Exploratory Data Analysis (EDA) - Water Potability Dataset

## Overview
This notebook conducts a rigorous **Exploratory Data Analysis (EDA)** on the [Water Potability](https://www.kaggle.com/datasets/adityakadiwal/water-potability/data) dataset. The ultimate goal of analyzing this dataset is to understand the biophysical and chemical characteristics of water samples and determine if they are safe for human consumption (**Potability**).

## Key Objectives
1. **Data Integrity & Missing Value Evaluation:** Analyze the presence and distribution of missing values across features like `ph`, `Sulfate`, and `Trihalomethanes` and determine the trade-offs of handling them.
2. **Univariate Feature Analysis:** Map out distributions, skewness, noise, and outliers for each of the 9 water quality metrics.
3. **Multivariate & Correlation Investigation:** Inspect pairwise feature relationships using interactive/static scatter plots and correlation matrices to identify predictive patterns.

## Summary of Key Insights from EDA
* **Missing Values Impact:** Approximately **38.6% of the samples (1,265 rows)** contain at least one missing value. Completely dropping these records leaves 2,011 complete rows.
* **Feature Distributions:** Most physical/chemical properties (like `ph`, `Hardness`, `Chloramines`, `Sulfate`, `Organic_carbon`, `Trihalomethanes`, and `Turbidity`) closely follow a **normal distribution** with varying degrees of noise and localized outliers. `Solids` and `Conductivity` exhibit noticeable **positive skewness**.
* **Imbalanced Target:** The target variable `Potability` is imbalanced, with fewer drinkable (potable) samples than non-potable ones.
* **Statistical Independence:** Pairwise scatter plots (including a 3D visualization) and the correlation matrix confirm that **there are virtually no linear or non-linear correlations** between the features. Features act as statistically independent variables, implying that simple linear classifiers might struggle and more robust non-linear models may be needed.
