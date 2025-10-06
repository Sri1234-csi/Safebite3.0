# Safebite3.0
just backend version
# Food Alertness App

This repo contains a minimal fullstack prototype for food logging, calorie scanning, OCR-ing medical reports, and ML-based cause & weekly risk predictions.

## Quick start (backend)
```bash
cd backend
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
# optional: download Kaggle data (ensure ~/.kaggle/kaggle.json is present)
python dataset/fetch_kaggle_data.py
# train (uses dataset/ if available, otherwise sample_events.csv)
python ml/train_tabular.py --data ../dataset --out ../models
python ml/train_timeseries.py --out ../models
# start the Flask backend
python app.py
