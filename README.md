# Predicting NBA MVP Performance

This repository contains the code and analysis for predicting the performance of NBA MVPs (Most Valuable Players). The project focuses on analyzing historical player statistics to identify factors influencing their points per game (PTS) and evaluate various predictive models.

---

## Project Overview

The objective of this project is to predict the points per game (PTS) of NBA MVPs based on historical data and explore the relationships between different player metrics. The project is divided into three main phases:

1. **Data Gathering and Cleaning**: Import and clean raw data to prepare it for analysis.
2. **Exploratory Data Analysis (EDA)**: Explore the relationships between variables and visualize key insights.
3. **Model Construction and Evaluation**: Build and evaluate different regression models to determine the best predictive model for PTS.

---

## Dataset

The dataset used in this project includes 474 observations of MVPs with 21 variables, such as:

- **Rank**: MVP rank
- **Player**: Player's name
- **PTS**: Points per game
- **TRB**: Total rebounds per game
- **AST**: Assists per game
- **STL**: Steals per game
- **Year**: Year the MVP was earned

The full dataset is sourced from Kaggle and cleaned using R for analysis.

---

## Project Structure

```
├── data
│   ├── mvps_raw.csv               # Raw dataset
│   ├── mvps_cleaned.csv           # Cleaned dataset
├── scripts
│   ├── data_cleaning.R            # Script for data cleaning
│   ├── exploratory_analysis.R     # Script for EDA
│   ├── model_construction.R       # Script for model fitting
├── visuals
│   ├── eda_plots.png              # Plots from EDA
│   ├── model_comparisons.png      # Model performance comparisons
├── README.md                      # Project documentation
```

---

## Workflow

### 1. Data Cleaning
- Converted categorical variables to factors.
- Removed irrelevant columns (e.g., Player, Rank) to focus on impactful variables.
- Checked and confirmed no missing values.

### 2. Exploratory Data Analysis (EDA)
- Visualized distributions of key metrics like PTS and Age.
- Identified strong correlations between variables using correlation plots.
- Investigated variable interactions through scatterplots and pairwise relationships.

### 3. Model Construction
Four models were built and evaluated:

1. **Linear Regression**: A baseline model to understand linear relationships.
2. **Elastic Net Regression**: Combines L1 and L2 penalties for feature selection and regularization.
3. **Boosted Tree Model**: Uses gradient boosting to improve accuracy.
4. **Random Forest**: A robust tree-based model for capturing non-linear relationships.

---

## Results

### Model Performance Comparison

| Model           | RMSE  | R-squared |
|------------------|-------|-----------|
| Boosted Tree     | 3.08  | 0.631     |
| Random Forest    | 3.29  | 0.615     |
| Linear Regression| 3.74  | 0.475     |
| Elastic Net      | 3.74  | 0.472     |

The Boosted Tree model outperformed other models in both RMSE and R-squared metrics, making it the best model for predicting PTS.

### Key Insights
- **PTS** is strongly correlated with **Minutes Played (MP)** and **Win Shares (WS)**.
- Some metrics like **Blocks (BLK)** and **Rebounds (TRB)** show weaker relationships with PTS.

---

## How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/your-repo-name.git
   ```
2. Install the required R packages:
   ```R
   install.packages(c("tidyverse", "tidymodels", "corrplot", "randomForest", "xgboost"))
   ```
3. Run the scripts in sequence for cleaning, EDA, and modeling.

---

## Future Improvements
- Expand the dataset to include non-MVP players for broader analysis.
- Experiment with deep learning models for improved accuracy.
- Automate the workflow using tools like R Markdown or Jupyter Notebooks.

---
## Contributors
- **Yuelin Shen** - Data Analysis and Modeling
---
