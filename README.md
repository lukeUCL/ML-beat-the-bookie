# Beat the Bookie - Premier League Match Prediction

Machine learning models for predicting Premier League match outcomes, achieving **57.5% accuracy** vs bookmaker baseline of 53%.

## Overview

Combines recency-based features with advanced rating systems (ELO, PI, GAP) across multiple ML algorithms to predict football match results.

## Key Results

- **57.5% accuracy** with SVM + L2 regularization  
- **60+ engineered features** from rolling team performance averages
- **2,761 matches** validated (2017-2024 Premier League seasons)
- **Outperformed bookmakers** by 4.5 percentage points

## Models Tested

| Model | Accuracy | Notes |
|-------|----------|-------|
| SVM (L2) | 57.5% | Best overall performer |
| Random Forest | 55.2% | Good feature importance insights |
| LSTM | 53.8% | Temporal sequence modeling |
| Logistic Regression | 52.1% | Baseline comparison |
| KNN | 49.1% | Instance-based learning |

## Technical Stack

- **Data**: Web scraped from FBRef (shots, passes, defensive actions)
- **Features**: Rolling averages (1-5 games) + team rating systems  
- **ML**: Scikit-learn, TensorFlow, hyperparameter tuning via grid search
- **Validation**: 5-fold cross-validation

## Key Challenge

All models struggled with draw prediction due to class imbalance - draws are inherently harder to predict from statistical patterns alone.

## Usage

```bash
git clone https://github.com/lukeUCL/ML-beat-the-bookie.git
cd ML-beat-the-bookie
pip install -r requirements.txt
python train_model.py
```

*UCL Computer Science coursework demonstrating ML applications in sports analytics.*
