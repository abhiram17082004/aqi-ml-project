Air Quality Index (AQI) Prediction using Hybrid AirPhy–ML Models
📌 Project Overview

Air pollution is a critical environmental and public health challenge, especially in rapidly urbanizing regions. This project focuses on accurate prediction of Air Quality Index (AQI) using a hybrid modeling framework that combines ensemble machine learning techniques with physics-guided neural network concepts (AirPhy).

The project evaluates multiple modeling approaches and proposes two advanced hybrid solutions that improve prediction accuracy, robustness, and generalization on real-world air quality data collected across Indian cities.

🎯 Objectives

Predict AQI using historical air pollutant data

Compare ensemble ML, deep learning, and physics-guided approaches

Design hybrid models that balance accuracy, interpretability, and computational efficiency

Identify key drivers influencing AQI through feature importance analysis

📊 Dataset

Source: Kaggle

Dataset: Air Quality Data in India

Link: https://www.kaggle.com/datasets/rohanrao/air-quality-data-in-india

Dataset Characteristics

Data from multiple Indian cities

Daily measurements from 2015 to 2020

Pollutants include PM2.5, PM10, NO, NO₂, NOx, NH₃, CO, SO₂, and O₃

AQI provided as the target variable

🧹 Data Preprocessing

The preprocessing pipeline ensures data consistency and reliability:

City-wise temporal interpolation for missing values

Forward and backward filling for short gaps

Median imputation for residual missing entries

Removal of samples with missing AQI values

Z-score normalization applied to continuous features

Time-aware train–test split to preserve temporal order

🛠️ Feature Engineering

To enhance predictive performance, extensive feature engineering was performed:

Temporal Features

Year, Month, Day

Day of Week, Week of Year, Quarter

Seasonal categories (Winter, Spring, Summer, Autumn)

Historical AQI Features

Lag features (1-day, 3-day, 7-day)

Rolling mean and rolling standard deviation (3, 7, 14 days)

Pollutant Interaction Features

PM2.5 / PM10 ratio

NO₂ / NO ratio

A total of 38 engineered features were used for model training.

🤖 Models Implemented
Ensemble Machine Learning Models

Random Forest

XGBoost

LightGBM

Gradient Boosting

Deep Learning Models

LSTM

GRU

Bidirectional LSTM

Physics-Guided Model

AirPhyNet (incorporating atmospheric diffusion and advection constraints)

🚀 Proposed Hybrid Approaches
1️⃣ Weighted Multi-Model Ensemble

This approach learns optimal non-negative weights for multiple base models instead of simple averaging. The weighting process:

Enhances strong predictors

Suppresses redundant or weak models

Improves accuracy without increasing training cost

This method offers an excellent balance between performance and computational efficiency.

2️⃣ Hybrid Random Forest–AirPhy Model

This hybrid architecture combines:

Random Forest for strong statistical learning on engineered features

AirPhy-based neural network to learn structured residual corrections

The final prediction is obtained by refining Random Forest outputs using physics-guided residual learning, improving performance especially under extreme AQI conditions.

📈 Evaluation Metrics

Model performance is evaluated using:

Mean Absolute Error (MAE)

Root Mean Squared Error (RMSE)

Mean Absolute Percentage Error (MAPE)

R² Score (primary metric)

🔍 Key Insights

Ensemble machine learning models outperform deep learning models on structured air quality data

Feature engineering plays a dominant role in AQI prediction accuracy

Physics-guided learning is most effective when integrated with strong ML baselines

Hybrid models provide improved stability and interpretability over standalone approaches

🧰 Technologies Used

Python

NumPy

Pandas

Scikit-learn

XGBoost

LightGBM

TensorFlow / Keras

Matplotlib

Seaborn

Google Colab



## 📁 Project Structure

```text
.
├── Copy_of_final_pynb.ipynb
├── city_day.csv
├── requirements.txt
└── README.md
