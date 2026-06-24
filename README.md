# Insurance Premium Category Predictor

A learning project built to practice **FastAPI**, **Pydantic**, **machine learning model serving**, and **frontend-backend integration**.

The application predicts an insurance premium category based on user information such as age, BMI-related features, occupation, income, smoking status, and city tier.

## Purpose

This project was created primarily to:

* Practice FastAPI development
* Learn API request validation using Pydantic
* Understand ML model deployment workflows
* Build feature engineering pipelines
* Connect a machine learning backend with a Streamlit frontend

The goal was educational rather than creating a production-ready insurance system.

---

## Features

### Backend (FastAPI)

* REST API endpoint for predictions
* Input validation using Pydantic
* Computed features:

  * BMI
  * Age Group
  * Lifestyle Risk
  * City Tier
* Machine learning inference using a trained model
* JSON responses

### Frontend (Streamlit)

* Simple user interface
* Form-based data entry
* API integration
* Prediction display

### Machine Learning

* Random Forest Classifier
* Feature engineering pipeline
* One-hot encoding for categorical features
* Model serialization using Pickle

---

## Project Structure

```text
├── insurance.py          # FastAPI application
├── frontend.py           # Streamlit frontend
├── insurance_demo.py     # Model training workflow
├── insurance.csv         # Dataset
├── model.pkl            # Trained model
└── README.md
```

## Engineered Features

The API derives additional features before inference:

### BMI

```python
BMI = weight / height²
```

### Age Group

* Young
* Adult
* Middle-aged
* Senior

### Lifestyle Risk

Based on smoking status and BMI.

### City Tier

Cities are mapped into Tier 1, Tier 2, or Tier 3 categories.

---

## Tech Stack

* Python
* FastAPI
* Pydantic
* Scikit-learn
* Pandas
* Streamlit

---

## Running the Project

### Install Dependencies

```bash
pip install fastapi uvicorn pandas scikit-learn streamlit
```

### Start FastAPI Server

```bash
uvicorn insurance:app --reload
```

### Launch Streamlit Frontend

```bash
streamlit run frontend.py
```

---

## Example API Request

```json
{
  "age": 30,
  "weight": 70,
  "height": 1.75,
  "income_lpa": 10,
  "smoker": false,
  "city": "Mumbai",
  "occupation": "private_job"
}
```

---

## Learning Outcomes

Through this project I practiced:

* FastAPI fundamentals
* API design and validation
* Feature engineering
* Model serialization and loading
* Backend/frontend integration
* ML inference pipelines

---

## Limitations

This project is intentionally educational and has several limitations:

* The dataset is AI-generated and does not represent real-world insurance data.
* Predictions should not be used for actual insurance decisions.
* The model was trained for learning purposes only.
* No production deployment, monitoring, security, or scalability considerations were implemented.
* The project does not claim novelty or research contribution.

---

## Disclaimer
This repository is a learning exercise created to practice FastAPI and machine learning deployment concepts. The dataset and outputs are synthetic and should not be interpreted as real insurance pricing recommendations.
This repository is a learning exercise created to practice FastAPI and machine learning deployment concepts. The dataset and outputs are synthetic and should not be interpreted as real insurance pricing recommendations.
