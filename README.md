# 🍃 STEMS — Smart Tea Estate Management System

STEMS is a machine learning-powered decision support system built for **Vellai Oya Tea Estate** in Hatton, Sri Lanka. It helps estate managers move away from guesswork and traditional practices toward smarter, data-driven decisions covering everything from when to fertilize to when to harvest.

🔗 **Frontend:** https://smart-tea-estate-management-system.streamlit.app
🔗 **Backend API:** https://minuka-stems-backend.hf.space/docs

---

## What It Does

| Module | Description |
|---|---|
| 🌱 **Fertilizer Scheduling** | Predicts how much fertilizer to apply and when, based on climate, yield history, plucking rounds, and past applications |
| 🧪 **Soil Quality** | Tracks and predicts soil pH and carbon levels over time, with actionable improvement suggestions |
| 📈 **Production Analytics** | Forecasts monthly yield using workforce and climate data, with year-on-year trend comparisons |
| 🌿 **Harvest Readiness** | Predicts the best time to pluck for maximum leaf quality and yield |

---

## Tech Stack

**Frontend**
- [Streamlit](https://streamlit.io/) — web UI
- Plotly — interactive charts
- Pandas — data processing

**Backend**
- [FastAPI](https://fastapi.tiangolo.com/) — REST API
- XGBoost / CatBoost / SVR — ML models
- Uvicorn — ASGI server
- Hosted on [Hugging Face Spaces](https://minuka-stems-backend.hf.space/docs)

---

## Project Structure

```
STEMS/
├── Backend/
│   ├── models/                         # Trained ML model files (.pkl, .json)
│   ├── main.py                         # FastAPI app
│   ├── Dockerfile
│   ├── requirements.txt
│   └── README.md
│
├── Data/                               # Raw estate datasets
│   ├── Block_Metadata.csv
│   ├── Climate_Data.csv
│   ├── EstateDataset.csv
│   ├── Fertilizer_History.csv
│   ├── ProductionForecastingDataset.csv
│   └── ...
│
├── Frontend/
│   ├── datasets/                       # Data files used by the frontend
│   ├── pages/
│   │   ├── Fertilizer_Schedule.py
│   │   ├── Harvest_Readiness.py
│   │   ├── Production_Analytics.py
│   │   ├── Soil_Quality.py
│   │   └── about.py
│   ├── app.py                          # Main Streamlit entry point
│   ├── shared.py                       # Shared UI components and colors
│   ├── api_client.py                   # Backend API calls
│   └── requirements.txt
│
├── Notebooks/                          # EDA and model training notebooks
│   ├── EDA.ipynb
│   ├── FertilizerSchedule.ipynb
│   ├── Soil_Quality_Analysis_and_Predictive_Model.ipynb
│   └── ...
│
└── README.md
```

---

## Getting Started

### Prerequisites
- Python 3.10+
- pip

### Run the Frontend

```bash
cd Frontend
pip install -r requirements.txt
streamlit run app.py
```

### Run the Backend locally

```bash
cd Backend
pip install -r requirements.txt
uvicorn main:app --reload
```

The backend API docs are available at [`/docs`](https://minuka-stems-backend.hf.space/docs).

---

## Deployment

| | |
|---|---|
| **Frontend** | [smart-tea-estate-management-system.streamlit.app](https://smart-tea-estate-management-system.streamlit.app) |
| **Backend** | [minuka-stems-backend.hf.space/docs](https://minuka-stems-backend.hf.space/docs) |

---

## Estate

| | |
|---|---|
| **Estate** | Vellai Oya Tea Estate |
| **Location** | Hatton, Sri Lanka |
| **Version** | STEMS v1.0 · 2026 |