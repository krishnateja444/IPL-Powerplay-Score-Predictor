# IPL Powerplay Score Predictor

## Overview

This project predicts IPL powerplay (first 6 overs) scores using machine learning and ball-by-ball match data. The model leverages cricket-specific feature engineering, Bayesian-smoothed encodings, and temporal weighting to estimate the final powerplay score based on the current match situation.

## Features

- Cricket-specific feature engineering
  - Dot balls
  - Boundaries
  - Early wickets
  - Run rate and momentum metrics
- Bayesian-smoothed target encoding for categorical variables
- Temporal weighting to prioritize recent matches
- Correlation and multicollinearity analysis using VIF
- Hyperparameter tuning with GridSearchCV
- Ridge Regression for robust score prediction

## Tech Stack

- Python
- Pandas
- NumPy
- Scikit-Learn
- StatsModels
- Matplotlib
- Seaborn

## Project Workflow

1. Data Collection & Cleaning
2. Feature Engineering
3. Exploratory Data Analysis
4. Bayesian Feature Encoding
5. Temporal Weighting
6. Correlation & VIF Analysis
7. Model Training
8. Hyperparameter Tuning
9. Model Evaluation

## Dataset

The model is trained on IPL ball-by-ball match data from multiple seasons.

### Input Features

Examples include:

- Batting Team
- Bowling Team
- Venue
- Current Score
- Wickets Lost
- Dot Ball Percentage
- Boundary Count
- Extras
- Momentum Metrics

### Target

- Predicted Powerplay Score (after 6 overs)

## Model

The final model uses **Ridge Regression** with optimized hyperparameters obtained through Grid Search.

## Results

Performance metrics obtained on the test set:

| Metric | Value |
|----------|----------|
| RMSE | XX.XX |
| MAE | XX.XX |
| R² Score | XX.XX |

## Repository Structure

```
IPL-Powerplay-Score-Predictor/
│
├── IPL_Powerplay_Score_Predictor.ipynb
├── README.md
├── requirements.txt
```

## Future Improvements

- Random Forest Regressor
- XGBoost Regressor
- Streamlit Web Application
- Live Match Prediction Dashboard
- SHAP-based Model Explainability
