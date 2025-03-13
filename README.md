# weather-trend-forecasting
AI-powered weather forecasting using ML & time-series analysis.

## 📌 Project Overview
This project analyzes global weather trends using **time-series forecasting** and **machine learning models**.  
It leverages **ARIMA, Holt-Winters, and Ensemble Models** to predict temperature variations.  
Additionally, it includes **anomaly detection, feature importance analysis, and spatial weather pattern visualization**.

---

## 🚀 Key Features
✔ **Data Cleaning & Preprocessing:** Handling missing values, outliers, and normalizing data.  
✔ **Exploratory Data Analysis (EDA):** Visualizing correlations, temperature trends, and precipitation patterns.  
✔ **Forecasting Models:** ARIMA, Holt-Winters, and an **ensemble** of both models.  
✔ **Anomaly Detection:** Detecting irregular temperature fluctuations.  
✔ **Feature Importance Analysis:** Identifying top contributors to weather variations using Random Forest.  
✔ **Spatial Analysis:** Mapping global temperature distributions with GeoPandas.  

---

## 🗂️ Dataset
**Dataset Name:** Global Weather Repository  
📌 **Source:** [Kaggle - Global Weather Repository](https://www.kaggle.com/datasets/nelgiriyewithana/global-weather-repository)  
📊 **Features:** 40+ features including temperature, humidity, wind speed, air quality, and more.  
⏳ **Time-Series Index:** `last_updated` (DateTime format)  

---

## 🔬 Data Processing & EDA
### ✅ Steps Taken:
- Converted `last_updated` to **DateTime format** for time-series analysis.
- **Removed outliers** using **Z-score filtering (threshold = 3)**.
- **Normalized numerical features** with **MinMaxScaler**.
- **Performed EDA** to analyze temperature trends, air quality impact, and global patterns.
- **Generated visualizations:**
  - 📌 **Correlation Heatmap**
  - 🌡️ **Temperature & Precipitation Trends**
  - 📊 **Boxplots for Weather Features**
  - 🌍 **Global Temperature Distribution Map**
  - 🚨 **Temperature Anomalies Over Time**

---

## 📈 Forecasting Models
### ✅ Implemented Models:
| Model | Description | Mean Squared Error (MSE) |
|--------|-------------|-------------------------|
| **ARIMA** | Time-series statistical forecasting | `0.021` |
| **Holt-Winters** | Seasonal exponential smoothing | `0.0209` |
| **Ensemble (ARIMA + Holt-Winters)** | Combination of both for better accuracy | **`0.0209`** |

✔ **The Ensemble Model provided the best accuracy, reducing error effectively.**  

---

## 📊 Advanced Analysis
### ✅ **Anomaly Detection**
- Used **Isolation Forest** (`contamination=0.01`) to identify unusual temperature spikes/drops.
- Found **significant anomalies** in August & winter months.

### ✅ **Feature Importance**
- Trained **Random Forest Regressor** to analyze which weather parameters impact temperature the most.
- **Top Features:**  
  1️⃣ **Air Quality (CO, NO2)**  
  2️⃣ **Latitude & Wind Speed**  
  3️⃣ **UV Index & Cloud Coverage**  

### ✅ **Spatial Analysis**
- Mapped **global temperature variations** using **GeoPandas & Matplotlib**.
- Found that **equatorial regions are consistently warmer**, while **high-latitude areas remain colder**.

---

## ⚙️ How to Run the Project
### 📌 **Using Google Colab (Recommended)**
1️⃣ **Upload `weather_forecasting.ipynb`** to **Google Colab**.  
2️⃣ **Ensure required dependencies are installed**:
   ```sh
   !pip install pandas numpy matplotlib seaborn scikit-learn statsmodels geopandas
   ```
### 3️⃣ Run all cells in the notebook.

## 📌 Running Locally

### 1️⃣ Clone this repository:
```sh
git clone https://github.com/rishi02102017/weather-trend-forecasting.git
cd weather-trend-forecasting
```
### 2️⃣ Install dependencies:
   pip install -r requirements.txt

