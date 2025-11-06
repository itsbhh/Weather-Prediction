#  Weather Prediction

## Overview
This project predicts **temperature trends** from the [*Seattle Weather Dataset*](https://www.kaggle.com/datasets/ananthr1/weather-prediction) using various **Deep Learning models** such as RNN, LSTM, GRU, CNN, and hybrid architectures.

---

## Steps

1. **Data Loading & Cleaning**
   - Uploaded `seattle-weather.csv` using Google Colab.
   - Checked for null and duplicate values.

2. **Preprocessing**
   - Extracted temperature column.
   - Created sequences using a sliding window of size **10**.
   - Split data into **Train (0–800)**, **Validation (800–1000)**, and **Test (1000–end)**.

3. **Models Implemented**
   - Vanilla RNN  
   - LSTM  
   - GRU  
   - CNN  
   - GRU–LSTM  
   - BiGRU–RNN  
   - BiGRU–LSTM  
   - CNN–BiGRU

4. **Training Setup**
   - Optimizer: `Adam`
   - Loss: `Mean Squared Error`
   - Callback: `EarlyStopping`
   - Evaluation Metrics: **RMSE**, **MAE**, **MAPE**

---

## Leaderboard

| Model       | Val RMSE | Val MAE | Val MAPE (%) | Test RMSE | Test MAE | Test MAPE (%) |
|--------------|-----------|----------|---------------|------------|-----------|----------------|
| **CNN–BiGRU** | **3.0223** | 2.4011 | 11.55 | **2.8307** | 2.2344 | 17.14 |
| LSTM         | 3.1211 | 2.4869 | 11.89 | 2.9067 | 2.2518 | 16.70 |
| GRU          | 3.1279 | 2.4717 | 11.78 | 2.9562 | 2.3270 | 18.48 |
| GRU–LSTM     | 3.1291 | 2.4756 | 11.89 | 2.9431 | 2.3208 | 18.00 |
| BiGRU–LSTM   | 3.1724 | 2.5095 | 12.04 | 2.9315 | 2.3099 | 17.33 |
| BiGRU–RNN    | 3.1732 | 2.5079 | 11.77 | 2.9713 | 2.3216 | 16.99 |
| Vanilla RNN  | 3.2492 | 2.5888 | 12.34 | 3.0890 | 2.4116 | 18.28 |
| CNN          | 3.9368 | 3.1126 | 14.65 | 3.3293 | 2.6859 | 21.48 |
<img width="609" height="268" alt="image" src="https://github.com/user-attachments/assets/e6b0a3db-5686-41da-ac0a-e189151f2699" />

---

## Best Model
**Model:** CNN–BiGRU  
**Validation RMSE:** 3.0223  
**Test RMSE:** 2.8306  

The **CNN–BiGRU** hybrid model performed best, effectively capturing both **local temporal features (CNN)** and **long-term dependencies (BiGRU)** in weather data.

---

## Visualizations
- Training vs Validation Loss for all models.  
- Actual vs Predicted temperature for validation and test sets.

---

## Conclusion
The **CNN–BiGRU** model outperformed others with the lowest RMSE and strong generalization on unseen data, making it most suitable for temperature forecasting.

