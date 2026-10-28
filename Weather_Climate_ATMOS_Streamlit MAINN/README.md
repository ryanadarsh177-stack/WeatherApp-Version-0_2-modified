# ATMOS — Weather & Climate Intelligence

A Streamlit app combining live weather lookup with an educational climate-regression experiment.

## Features
- Animated, responsive dark dashboard with gradient/glass styling.
- City search and current conditions through the Open-Meteo APIs.
- Five-day temperature outlook.
- Linear Regression models estimating rainfall and sea-level rise from average temperature and per-capita CO₂ emissions.
- Test-set RMSE and R², interactive Plotly charts, dataset preview, and cleaned CSV download.
- Bundled dataset so the climate lab works immediately; optional CSV upload for a compatible dataset.

## Deploy on Streamlit Community Cloud
1. Upload `app.py`, `requirements.txt`, the `data/` folder, and this README to a GitHub repository. Keep the `data` folder and its CSV together.
2. In Streamlit Community Cloud, create an app from that repository and select `app.py` as the main file.
3. Deploy. Streamlit installs dependencies from `requirements.txt` automatically.

## Run locally (optional)
```bash
python -m pip install -r requirements.txt
python -m streamlit run app.py
```

## Dataset requirements for an uploaded CSV
The app expects these columns:
- `Avg Temperature (°C)`
- `CO2 Emissions (Tons/Capita)`
- `Rainfall (mm)`
- `Sea Level Rise (mm)`

Other columns are optional.

## Important limitations
Predictions are educational estimates only. The bundled dataset is small and observational; linear regression with two inputs does not capture the complex physics and geography needed for reliable climate forecasts. RMSE is reported in the units of each target. Weather lookup requires internet access.
