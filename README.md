# final_submission_wids
final submission for the project Predicting Stock Volatility Using Financial News Sentiment Analysis

# WiDS Project: News Sentiment-Based Stock Movement Prediction

## Overview
This project was developed as part of the **Women in Data Science (WiDS)** program.  
The goal of the project is to explore whether **financial news sentiment** can be used to predict **next-day stock price movement** using machine learning models.

The project covers the **complete data science pipeline**, including data collection, preprocessing, feature engineering, model training, evaluation, and interpretation of results.

---

## Problem Statement
Predict whether a stock’s closing price will **increase or decrease on the next trading day** based on aggregated sentiment extracted from financial news headlines.

This is framed as a **binary classification problem**:
- `1` → Price goes up
- `0` → Price goes down or remains the same

---

## Dataset Description
The project uses two primary data sources:

### 1. Financial News Data
- Collected using RSS feeds (MarketWatch, CNBC)
- Contains news headlines, publication dates, and source
- Sentiment extracted from headlines using polarity-based sentiment analysis

### 2. Stock Price Data
- Downloaded using `yfinance`
- Includes Open, High, Low, Close, Volume
- Target variable created using next-day closing price

---

## Feature Engineering
Sentiment features were aggregated on a **daily basis**, including:
- `sentiment_score` – average daily sentiment
- `positive_count` – number of positive headlines
- `negative_count` – number of negative headlines
- `neutral_count` – number of neutral headlines

These features were merged with stock price data using a **date-based join**.

---

## Models Implemented
The following machine learning models were trained and evaluated:

1. **Logistic Regression**
   - Used as a baseline model
   - Simple and interpretable

2. **Random Forest Classifier**
   - Tree-based ensemble method
   - Helps capture non-linear relationships

3. **XGBoost Classifier**
   - Gradient boosting model
   - Provided the best overall performance

---

## Model Evaluation
- **Time-based train-test split** was used to prevent data leakage
- Evaluation metrics:
  - Accuracy
  - Precision
  - Recall
  - F1-score
- Models were compared using a summary results table

---

## Results and Insights
- XGBoost outperformed Logistic Regression and Random Forest
- Ensemble methods captured complex patterns better than linear models
- News sentiment showed predictive value, but performance is limited by market noise
- Time-based validation is critical for financial prediction tasks

---

## Files in This Repository
- `midsem_submission.ipynb`  
  → Complete Jupyter Notebook with data preparation, modeling, and evaluation

- `news_raw.csv`  
  → Raw scraped news data

- `news_cleaned.csv`  
  → Cleaned and preprocessed news data

- `merged_midterm_data.csv`  
  → Final merged dataset with sentiment and stock data

- `WiDS_Final_Report.pdf`  
  → Detailed report explaining learnings and experiments throughout WiDS

- `README.md`  
  → Project documentation

---

## Tools and Libraries Used
- Python
- pandas, numpy
- scikit-learn
- xgboost
- yfinance
- BeautifulSoup
- TextBlob
- matplotlib

---

## Conclusion
This project demonstrates the application of machine learning techniques to real-world financial data.  
Through WiDS, I gained hands-on experience in building end-to-end ML pipelines, handling noisy data, and evaluating models realistically.

---

## Author
**Aryan**  
WiDS Program Participant
