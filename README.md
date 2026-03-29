# Student Performance: Feature Selection (Lasso Regression) 

> **Objective:** To identify the most significant demographic and academic predictors of student success using Lasso Regression, and to evaluate the performance trade-offs between a high-dimensional complex model and a simple baseline model.

## Overview
This repository contains a regression analysis focusing on **Feature Selection**. Using a dataset of secondary school student performance, the project implements `LassoCV` to penalize and eliminate non-contributing variables from a large pool of socio-economic and behavioral features. 

The core insight of this study demonstrates that while Lasso successfully identified statistically significant factors (like maternal education and absences), a simple baseline model relying strictly on past academic performance (G1 and G2 grades) ultimately achieved a lower RMSE and higher R² score. This highlights the vital data science principle of model parsimony: more features do not inherently yield better predictive power.

**A full summary of the correlation analysis, selected features, and model performance metrics is available in the included PDF Analysis Report.**

## Dataset
* **Source File:** `student-mat-converted.csv`
* **Target Variable:** `G3` (Final Grade, continuous numerical)
* **Features Analysed:** 30+ socio-economic, demographic, and academic variables (e.g., `Medu`, `absences`, `failures`, `G1`, `G2`).

## Repository Structure
* **`Feature_Selection_Analysis_Report.pdf`**: The formal documentation detailing the EDA, the features selected by the Lasso algorithm, and the final RMSE/R² comparisons.
* **`Feature_Selection_Lasso_Regression.ipynb`**: The core Jupyter Notebook containing the data preprocessing (`pd.get_dummies`), correlation heatmaps, Lasso implementation, and baseline model training.
* **`student-mat-converted.csv`**: The dataset used for training and evaluation.

## Tech Stack
* **Language:** Python
* **Data Preprocessing:** Pandas (One-Hot Encoding via `get_dummies`)
* **Machine Learning:** Scikit-Learn (`LassoCV`, `LinearRegression`, `StandardScaler`)
* **Statistical Visualization:** Seaborn (`histplot`, `barplot`), Matplotlib

## How to Run the Notebook

### Run in Cloud (Recommended)
You can view and execute the code instantly in your browser via Google Colab:
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ronanpatrick/lasso-feature-selection-student-performance/blob/main/Feature_Selection_Lasso_Regression.ipynb)

*(Note: If running in Colab, please ensure you upload `student-mat-converted.csv` to your session storage first).*

### Run Locally
1. Clone this repository: `git clone https://github.com/ronanpatrick/lasso-feature-selection.git`
2. Install the required libraries: `pip install pandas numpy scikit-learn matplotlib seaborn`
3. Open the `.ipynb` file in Jupyter Notebook or VS Code and execute the cells.
