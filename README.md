MTN Customer Churn Prediction

A production-style machine learning pipeline to predict customer churn, deployed as a live Streamlit web application.

Live Demo

👉 https://mtn-customer-churn-analysis-and-prediction-jxwu6jccza6hbhs7jnq.streamlit.app/

Project Overview

This project builds an end-to-end ML pipeline on a simulated MTN-style telecom dataset. The goal is to predict whether a customer is likely to churn based on their profile and usage behaviour.

##Pipeline Structure


Customer Churn/
├── src/
│   ├── data_ingestion.py        # Load and validate raw data
│   ├── data_cleaning.py         # Handle missing values, outliers
│   ├── eda.py                   # Exploratory data analysis & visualizations
│   ├── feature_engineering.py   # Encoding, scaling, feature creation
│   ├── model_building.py        # Train multiple ML models
│   ├── model_evaluation.py      # Evaluate and compare models
│   ├── hyperparameter_tuning.py # Optimize best model
│   └── utils.py                 # Helper functions
├── models/                      # Saved model files (.pkl)
├── results/                     # CSV comparison reports
├── plots/                       # Generated visualizations
├── app.py                       # Streamlit application
├── main.py                      # Pipeline entry point
└── requirements.txt


##Models Trained

	•	Logistic Regression
	•	Random Forest
	•	Gradient Boosting ✅ (best performer)
	•	XGBoost

##Tech Stack

	•	Python 3.14
	•	Scikit-learn
	•	XGBoost
	•	Pandas & NumPy
	•	Matplotlib & Seaborn
	•	Streamlit

##How to Run Locally

# Clone the repo
git clone https://github.com/ayomide-williams/mtn-customer-churn-analysis-and-prediction.git

# Navigate to project folder
cd mtn-customer-churn-analysis-and-prediction

# Create virtual environment
py -m venv .venv
.venv\Scripts\activate.bat

# Install dependencies
pip install -r requirements.txt

# Run the pipeline
python main.py

# Launch the app
streamlit run app.py

##Results

|Model              |F1-Score|Accuracy  |
|-------------------|--------|----------|
|Gradient Boosting  |Best    |✅ Selected|
|XGBoost            |2nd     |-         |
|Random Forest      |3rd     |-         |
|Logistic Regression|4th     |-         |

Fill in your actual scores from results/final_model_comparison.csv

Author

Ayomide Williams
Electrical Engineer | Data Scientist
