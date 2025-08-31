Google-Play-Store-Apps-Rating-Prediction

This project predicts Google Play Store app ratings using data analysis and machine learning.
The dataset contains details of apps such as category, size, installs, type (free/paid), price, and reviews.

---

Dataset

Records: 10,000 apps ,
Columns:
App: App name ,
Category: App category (Games, Tools, Family, etc.) ,
Rating: Target variable (1–5 scale) ,
Reviews: Number of user reviews ,
Size: App size (cleaned to MB) ,
Installs: Install counts (converted to integers) ,
Type: Free/Paid ,
Price: Price in USD (cleaned) ,
Content Rating: Audience type (Everyone, Teen, etc.) ,
Genres: App genre ,
Metadata (Last Updated, Current Ver, Android Ver).

---

Workflow

1. Data Cleaning & Preprocessing:
Removed duplicates & missing values ,
Converted Size, Installs, Price to numeric ,
Encoded categorical features ,
Feature engineering: Log_Reviews, Price_Bucket, Install_Bucket.

2. Exploratory Data Analysis (EDA):
Ratings distribution: Most apps score between 4.0–4.5 ,
Top categories: Family, Games, Tools ,
Free vs Paid: 92% apps are free, but paid apps have higher ratings ,
Installs: Most under 1M, few over 500M ,
Content Rating: Mostly “Everyone”.

3. Sentiment Analysis:
Ratings converted to sentiment classes:
Positive (≥4.0): ~85% ,
Neutral (3.0–3.9): ~10% ,
Negative (<3.0): ~5%.

4. Machine Learning Models:
Random Forest: R² ≈ 0.87 ,
Gradient Boosting: R² ≈ 0.85 ,
XGBoost: R² ≈ 0.89 (Best model) ,
SHAP analysis: Top predictors: Reviews, Installs, Category, Size.

---

Technologies Used:

Python 3.8+
Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn, xgboost, shap.
