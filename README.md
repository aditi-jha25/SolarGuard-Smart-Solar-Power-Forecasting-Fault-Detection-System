# Solar Power Generation Forecasting and Anomaly Detection

## Project Overview
This project predicts short-term solar power generation using machine learning and detects anomalies by comparing predicted and actual power output. The goal is to identify unusual deviations in solar energy production that may indicate weather variations or potential hardware issues.

The system trains multiple regression models using historical weather and time-based features. A stacking model combines predictions from base models to improve forecasting performance. Anomalies are detected by analyzing the prediction error between actual and predicted power.

---

## Features
- Predict solar power generation using machine learning
- Compare multiple regression models
- Improve prediction using a stacking ensemble
- Detect anomalies using prediction error
- Categorize anomalies based on error percentage
- Visualize predicted vs actual solar power

---

## Machine Learning Models

### Base Models
The following regression models are used for solar power prediction:

- **Random Forest Regressor**
- **K-Nearest Neighbors (KNN) Regressor**

### Ensemble Model
To improve prediction accuracy, a **Stacking Regressor** is used to combine predictions from the base models.

---

## Anomaly Detection

After predicting solar power generation, anomalies are detected using **residual error analysis**.

Error is calculated as:

Error = |Actual Power − Predicted Power|

If the error exceeds a threshold, the data point is marked as an anomaly.

---

## Anomaly Classification

Based on the error percentage, anomalies are categorized as:

| Error Percentage | Category |
|------------------|----------|
| < 10% | Normal |
| 10% – 25% | Weather Variation |
| > 25% | Possible Hardware Fault |
| Actual Power = 0 | Night / No Generation |

---

## Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

---

## Dataset

The dataset contains solar power generation data along with weather and environmental features such as:

- Temperature
- Humidity
- Sky Cover
- Wind Speed
- Visibility
- Time features (year, month, day, hour)

Target variable:
```
Power Generated
```

---

## Project Workflow

1. Data Preprocessing
2. Feature Selection
3. Model Training
   - Random Forest Regressor
   - KNN Regressor
4. Ensemble Learning using Stacking Regressor
5. Solar Power Prediction
6. Error Calculation
7. Anomaly Detection
8. Anomaly Classification
9. Visualization of Results

---

## Example Output

| Actual Power | Predicted Power | Error | Anomaly | Error % | Anomaly Type |
|--------------|----------------|-------|--------|--------|--------------|
| 0.598 | 0.571 | 0.026 | False | 4.38 | Normal |
| 0.306 | 0.264 | 0.041 | False | 13.61 | Weather Variation |
| 0.756 | 0.534 | 0.221 | True | 29.29 | Possible Hardware Fault |

---

## Future Improvements
- Use deep learning models such as LSTM for time-series forecasting
- Use real solar plant sensor data
- Implement advanced anomaly detection techniques
- Build a real-time monitoring dashboard

---

Clone the repository  
```bash
git clone <your-repo-link>
