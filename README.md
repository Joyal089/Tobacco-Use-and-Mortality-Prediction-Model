# Tobacco Use and Mortality Prediction Model

A data-science project on smoking statistics for England. It explores smoking-related deaths and hospital admissions, with the aim of predicting mortality from tobacco-use data.

## Data

Public, aggregated statistics (no individual-level data), in the `Tobacco Use and Mortality Prediction Model/` folder:

| File | Contents |
|---|---|
| `fatalities.csv` | Deaths attributable to smoking, by year, diagnosis (ICD-10) and sex |
| `admissions.csv` | Hospital admissions attributable to smoking |
| `smokers.csv` | Share of adults who smoke, by year, sex and age group (from 1974) |
| `prescriptions.csv` | Stop-smoking prescriptions (NRT, bupropion, varenicline) and their cost |
| `metrics.csv` | Tobacco prices, affordability and household spending |

These match the NHS England "Statistics on Smoking" tables, widely shared as a Kaggle dataset.

## What the notebook does

`Tobacco Use and Mortality Prediction Model.ipynb`:

1. Loads `fatalities.csv`, checks for missing values and forward-fills gaps
2. Summary statistics, histograms and a correlation heatmap
3. One-hot encodes sex and diagnosis, and prepares features and a target for modelling

`random_forest_model.pkl` and `scaler.pkl` are a saved Random Forest model and feature scaler from the modelling work.

## Tech

Python 3, pandas, NumPy, scikit-learn, seaborn, Matplotlib, Jupyter

## How to run

```bash
pip install pandas numpy scikit-learn seaborn matplotlib notebook
jupyter notebook
```

Open the notebook and change the `pd.read_csv(...)` path in the first cell to the `fatalities.csv` in this folder.

## Status and results

Work in progress. The exploration cells run. The last modelling cell stops with an error as saved (`y.value_counts()` is called on a NumPy array), so the notebook does not yet report model accuracy.
