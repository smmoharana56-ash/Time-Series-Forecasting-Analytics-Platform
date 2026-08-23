# 📈 Financial Time-Series Forecasting & Analytics Platform

An end-to-end machine learning platform designed to ingest financial stock market data, compute technical momentum indicators, train baseline time-series models (Facebook Prophet & Auto-ARIMA), perform 90-day holdout backtesting, serve REST API endpoints via FastAPI, and display dynamic insights on an interactive Plotly Dash web dashboard.

---

## 🏗️ Architecture Diagram
┌──────────────────────────────────────────────────────────┐
│ Phase 1: Data Ingestion & Technical Feature Engineering  │
│ ── Downloads Stock Data & Computes Indicators (RSI, SMA) │
└────────────────────────────┬─────────────────────────────┘
│
▼
┌──────────────────────────────────────────────────────────┐
│ Phase 2: Time-Series Model Training                      │
│ ── Fits Facebook Prophet & Auto-ARIMA Models             │
└────────────────────────────┬─────────────────────────────┘
│
▼
┌──────────────────────────────────────────────────────────┐
│ Phase 3: Holdout Backtesting Engine                      │
│ ── Evaluates Metrics (MAPE, RMSE, MAE) over 90 Days      │
└────────────────────────────┬─────────────────────────────┘
│
▼
┌──────────────────────────────────────────────────────────┐
│ Phase 4: REST API Integration (FastAPI)                  │
│ ── Exposes Endpoints (/tickers, /forecast, /metrics)│
└────────────────────────────┬─────────────────────────────┘
│
▼
┌──────────────────────────────────────────────────────────┐
│ Phase 5: Interactive Web UI (Plotly Dash)                │
│ ── Renders Interactive Graphs & Financial Performance    │
└──────────────────────────────────────────────────────────┘


---

## 🛠️ Tech Stack & Dependencies

* **Core Programming:** Python 3.10+
* **Data Manipulation & Storage:** `pandas`, `numpy`, `pyarrow` (Parquet Columnar Storage)
* **Forecasting Engines:** `prophet`, `pmdarima` (Auto-ARIMA)
* **Model Evaluation:** `scikit-learn` (MAPE, RMSE, MAE)
* **REST API Backend:** `fastapi`, `uvicorn`
* **Interactive Frontend:** `plotly`, `dash`

---

## 🚀 Setup & Installation Instructions

### 1. Clone the Repository
```bash
git clone [https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git](https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git)
cd Time-Series Forecasting & Analytics Platform
2. Set Up Virtual Environment
Bash
# On Windows
python -m venv venv
venv\Scripts\activate

###3. Install Required Dependencies
Bash
pip install pandas numpy prophet pmdarima scikit-learn fastapi uvicorn plotly dash pyarrow
4. Run the Pipeline & Applications
Phase 1 to 3 (Pipeline): Execute time series.ipynb to process stock data, generate predictions, and run backtesting into the ./data/ directory.

Phase 4 (FastAPI Backend):

Bash
python -m uvicorn app:app --reload
Interactive Swagger API documentation available at: http://127.0.0.1:8000/docs

Phase 5 (Dash Web UI): Run the notebook dashboard cell or execute:

Bash
python dashboard.py
