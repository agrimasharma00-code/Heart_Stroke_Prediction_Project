# Heart Disease Prediction App

This is a Streamlit web app that predicts the risk of heart disease using a trained machine learning model. The app collects basic health inputs such as age, blood pressure, cholesterol, heart rate, and ECG-related features, then uses a saved scaler and KNN model to produce a prediction.

The app uses the K-Nearest Neighbors (KNN) algorithm for prediction. User inputs are first scaled using the saved scaler, then passed into the trained KNN model to generate the result.

## Live Demo
https://heartstrokepredictionproject.streamlit.app/

## Features

- Clean Streamlit interface for quick predictions
- Uses a trained KNN model for inference
- Automatically scales input data before prediction
- Handles the required one-hot encoded feature columns for the model

## Inputs Used

- Age
- Sex
- Chest pain type
- Resting blood pressure
- Cholesterol
- Fasting blood sugar
- Resting ECG
- Maximum heart rate
- Exercise-induced angina
- Oldpeak
- ST slope

## Project Files

- [app.py](app.py) - Main Streamlit application
- [knn_heart_model.pkl](knn_heart_model.pkl) - Trained prediction model
- [heart_scaler.pkl](heart_scaler.pkl) - Feature scaler used before prediction
- [heart_columns.pkl](heart_columns.pkl) - Expected feature columns for the model

## Run Locally

1. Install the dependencies:

```bash
pip install streamlit pandas joblib scikit-learn
```

2. Start the app:

```bash
streamlit run app.py
```

3. Open the local URL shown in the terminal, usually:

```bash
http://localhost:8501
```


## Notes

- The model files must stay in the same folder as `app.py`.
- The prediction logic assumes the saved model and scaler were trained with the same feature layout used in the app.
