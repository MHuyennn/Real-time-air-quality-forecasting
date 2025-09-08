# Real-time air quality forecasting & dashboard  

## Introduction  
This project provides a real-time air quality monitoring and forecasting system, including:  

### Main Components  
- **FastAPI backend**: Connects to a MongoDB database and provides API endpoints.  
- **Streamlit dashboard**: Visualizes AQI through maps, charts, rankings, and short-term forecasts.  
- **Forecasting model**: Uses deep learning (PyTorch) to predict PM2.5, PM10, NO₂, CO, and O₃ levels up to 24 hours ahead.  
- **Health recommendations**: Provides alerts and suggests the best times for outdoor activities based on AQI levels.  

---

## Environment Setup  

### Requirements  
- Python 3.9 or higher  

### Installation  
```bash
pip install -r requirements.txt

# How to Run the Application  

## 1. Start the API backend (FastAPI)  
```bash
python main.py
The API will run at: http://localhost:8000/data

## 2. Start the Streamlit dashboard
streamlit run app.py
Open the browser at: http://localhost:8501

# Features
## Monitoring
- Display AQI levels on an interactive map.
- Rank the cleanest locations in real-time.
## Forecasting
- Predict AQI levels for each hour within the next 24 hours using the SOFTS model.
- Provide personalized health recommendations based on age, pre-existing conditions, outdoor duration, and activity intensity.
## Visualization
- Generate time-series charts for pollution indicators.

# Model Training
## Related Files
- exp_custom.py: Training pipeline for custom datasets.
- exp_long_term_forecasting.py: Training pipeline for benchmark datasets (ETT, Weather, Solar, PEMS...).
