# Weather Data Analysis & Temperature Prediction

This project analyzes historical weather data from Bangalore and predicts future temperature and humidity trends using **Linear Regression**. The dataset used is `Bangalore.csv`, which contains hourly weather measurements.

## 📈 Goals
- Explore and visualize temperature patterns
- Smooth noisy time-series data
- Build a regression model for forecasting
- Predict temperatures and relative humidity for the next 5 days (hourly)

## 📂 Project Structure
- `weather_prediction.ipynb`: Jupyter Notebook containing the data analysis, visualization, and prediction code.
- `Bangalore.csv`: Local dataset with historical weather data (not included in this repository).
- `README.md`: This file, providing an overview of the project.

## 🛠️ Requirements
To run the notebook, you need the following Python libraries:
- `pandas`
- `numpy`
- `matplotlib`
- `scikit-learn`

Install them using:
```bash
pip install pandas numpy matplotlib scikit-learn
```

## 📊 Dataset
The `Bangalore.csv` dataset includes the following key columns:
- `date`: Timestamp of the weather observation
- `temperature_2m`: Temperature at 2 meters above ground (°C)
- `relative_humidity_2m`: Relative humidity (%)
- `dew_point_2m`: Dew point temperature (°C)
- `pressure_msl`: Mean sea level pressure (hPa)
- `cloud_cover`: Cloud cover percentage (%)

Ensure the dataset is placed in the same directory as the notebook.

## 🔍 Methodology
1. **Data Loading & Preprocessing**:
   - Load the dataset and convert the `date` column to datetime.
   - Sort data by date and handle missing values.
   - Create time-based features (e.g., day of year, hour) and cyclic features for seasonality.

2. **Exploratory Data Analysis**:
   - Visualize raw and smoothed (7-day rolling average) temperature trends.
   - Analyze daily and annual temperature fluctuations.

3. **Temperature Prediction**:
   - Use Linear Regression with features like date, humidity, pressure, cloud cover, and cyclic time features.
   - Train/test split (80/20) with no shuffling to preserve temporal order.
   - Forecast hourly temperatures for the next 5 days.

4. **Humidity Prediction**:
   - Predict relative humidity using features like temperature, dew point, cloud cover, and pressure.
   - Generate a 5-day hourly forecast based on the last known state.

## 📈 Visualizations
The notebook includes the following plots:
- Raw hourly temperature over time
- Smoothed temperature trends (7-day rolling average)
- Actual vs. predicted temperatures on test data
- 5-day hourly temperature forecast
- 5-day hourly relative humidity forecast

## 🚀 Usage
1. Clone or download this repository.
2. Place the `Bangalore.csv` dataset in the project directory.
3. Open `weather_prediction.ipynb` in Jupyter Notebook or JupyterLab.
4. Run the cells sequentially to perform the analysis and generate predictions.

## 📝 Notes
- The model assumes the last 24 hours' weather patterns for non-time-based features in future predictions, which may oversimplify real-world variability.
- For improved accuracy, consider advanced models (e.g., ARIMA, LSTM) or incorporating real-time weather data.
- The dataset is not provided; users must supply their own `Bangalore.csv` with the expected format.

## 📬 Contact
For questions or suggestions, feel free to open an issue in the repository or contact the project maintainer.