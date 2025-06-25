# Red & White Wine Data Analysis

## Author

**Arjun Vijay Anup**

---

## Table of Contents

1. [Project Overview](#project-overview)  
2. [Data Description](#data-description)  
3. [Notebook Structure](#notebook-structure)  
4. [Installation & Dependencies](#installation--dependencies)  
5. [Usage](#usage)  
6. [Key Findings](#key-findings)  
7. [License](#license)  

---

## Project Overview

This Jupyter notebook performs an in-depth analysis of the Lisbon “Wine Quality” datasets (red and white) from the UCI Machine Learning Repository. It covers:

- **Exploratory Data Analysis (EDA)**  
- **Statistical Hypothesis Testing** (t-tests between red and white wines)  
- **Correlation Analysis** and visualizations  
- **Regression Modeling** to predict wine quality (linear regression, forward selection)  
- **Clustering** (k-means and alternative algorithm) to discover natural groupings  

The goal is to understand which physicochemical properties most influence perceived quality and to explore natural clusters within the data.

---

## Data Description

The analysis uses two CSV files:

- `winequality-red.csv` — 1,599 red wine samples  
- `winequality-white.csv` — 4,898 white wine samples  

A detailed description of each attribute (fixed acidity, volatile acidity, citric acid, residual sugar, chlorides, free sulfur dioxide, total sulfur dioxide, density, pH, sulphates, alcohol, quality) is provided in `wines.txt`.

> **Data source:**  
> P. Cortez, A. Cerdeira, F. Almeida, T. Matos and J. Reis. “Modeling wine preferences by data mining from physicochemical properties.” *Decision Support Systems*, vol. 47, no. 4, pp. 547–553, 2009. (UCI Machine Learning Repository)

---

## Notebook Structure

1. **Data Loading & Inspection**  
   - Read CSVs into pandas DataFrames  
   - Check for missing values and summary statistics  

2. **Exploratory Data Analysis**  
   - Numerical summaries & histograms  
   - Boxplots and scatter plots  

3. **Hypothesis Testing**  
   - Two-sample t-tests for each physicochemical measurement  
   - Visual comparison (side-by-side plots)  

4. **Combined Dataset & Correlation Analysis**  
   - Merge red and white into one DataFrame  
   - Pearson correlation matrix and strongest variable pairs  
   - Scatter plots for top correlations  

5. **Regression Modeling**  
   - Binarize quality into **Poor (0–5)** vs. **Good (6–10)**  
   - Standardize predictors  
   - Fit and interpret a linear regression  
   - Perform forward selection and compare  

6. **Clustering Analysis**  
   - K-means: elbow method to choose *k*  
   - Identify most discriminatory features  
   - Alternative clustering (e.g., hierarchical or DBSCAN) and comparison  

---

## Installation & Dependencies

1. **Clone the repository**  
   ```bash
   git clone https://github.com/<your-username>/wine-quality-analysis.git
   cd wine-quality-analysis
   ```

2. **Create a virtual environment** (recommended)  
   ```bash
   python3 -m venv venv
   source venv/bin/activate    # macOS/Linux
   venv\Scripts\activate     # Windows
   ```

3. **Install dependencies**  
   ```bash
   pip install -r requirements.txt
   ```
---

## Usage

1. **Ensure the data files** (`winequality-red.csv`, `winequality-white.csv`, and `wines.txt`) are in the project root.  
2. **Launch Jupyter**  
   ```bash
   jupyter notebook
   ```  
3. **Open** `wineDataAnalysis.ipynb` and run all cells in order.

---

## Key Findings

- **Red vs. White Wines:** Statistically significant differences (at α = 0.01) in acidity, sulphates, alcohol content, etc.  
- **Top Correlations:** Alcohol–quality and sulphates–quality showed the strongest positive relationships.  
- **Regression Model:** Alcohol content and volatile acidity were among the most predictive features.  
- **Clustering:** Optimal *k* (via elbow method) revealed distinct groups corresponding to quality and type; alternative clustering yielded comparable groupings with slightly different feature importance.

*(For full details and visualizations, see the notebook.)*

---
