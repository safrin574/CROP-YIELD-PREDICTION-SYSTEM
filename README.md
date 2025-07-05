
# 🌾 Crop Yield Prediction System

This project builds a machine learning pipeline using **Random Forest Regressor** to predict **crop yield (tons/hectare)** based on real-world agricultural data such as rainfall, temperature, soil type, and weather conditions.

---

## ✅ Problem Statement

Traditional methods of estimating crop yield are often manual, time-consuming, and inaccurate due to unpredictable environmental factors. This system aims to:

- Accurately predict crop yield using key environmental and soil-related features.
- Provide agricultural stakeholders with data-driven insights.
- Enable real-time prediction based on user input.

---

## 📁 Dataset

The dataset `crop.csv` includes the following columns:

- `Rainfall_mm`: Rainfall in millimeters
- `Temperature_Celsius`: Temperature in °C
- `Soil_Type`: Type of soil (e.g., Clay, Sandy, Loam)
- `Weather_Condition`: Weather status (e.g., Sunny, Rainy)
- `Fertilizer_Used`: Whether fertilizer was used
- `Irrigation_Used`: Whether irrigation was used
- `Yield_tons_per_hectare`: Crop yield in tons per hectare (target)

---

## 🔧 Technologies & Libraries Used

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Google Colab

---

## 🔍 Features & Workflow

### 📊 Data Preprocessing
- Removes missing values
- Handles outliers (Rainfall, Temperature)
- Creates new features:
  - `Rainfall_Temp_Interaction`
  - `Log_Rainfall`
  - `Rainfall_Category` (Binned category)

### 📈 Visualizations
- Correlation heatmap
- Box plots of yield by soil and weather
- Prediction scatter plot
- Error distribution
- Feature importance chart

### 🤖 Machine Learning Pipeline
- Splits dataset into training and testing sets
- Applies `StandardScaler` for numerical and `OneHotEncoder` for categorical features
- Trains a `RandomForestRegressor`
- Evaluates model using:
  - Mean Squared Error (MSE)
  - R² Score

### 👤 Interactive User Prediction
- Accepts real-time user input
- Predicts crop yield based on entered environmental conditions

---

## 📌 How to Run the Project

1. Open [Google Colab](https://colab.research.google.com/)
2. Upload `crop.csv` file when prompted
3. Run all the cells
4. Enter user input values when prompted for prediction

---

## 📷 Output Visuals

- `correlation_heatmap.png`
- `yield_by_soil_type.png`
- `yield_by_weather_condition.png`
- `crop_yield_prediction.png`
- `prediction_error.png`
- `feature_importance.png`

These files are saved automatically when you run the code.

---

## 📌 Sample Input for Prediction

```
Rainfall: 600
Temperature: 28
Soil Type: Loam
Weather: Sunny
```

📤 **Predicted Crop Yield:** `4.73 tons/ha` (example)

---

## 📚 Future Enhancements

- Include fertilizer and irrigation effects as predictors
- Incorporate seasonality and region-specific crop data
- Train ensemble models (XGBoost, LightGBM) for comparison
- Deploy model via web interface (Streamlit/Flask)


