# Exoplanet Analysis

This repository contains analyzed exoplanet data from the NASA Kepler mission to predict potential habitability using a logistic regression model.

## Dataset
- **Source:** NASA Exoplanet Archive (Cumulative KOI Table)
- **Citation:** NASA Exoplanet Archive. (2025). *Cumulative Kepler Object of Interest (KOI) table* [Data set]. NASA Exoplanet Science Institute. https://exoplanetarchive.ipac.caltech.edu/cgi-bin/TblView/nph-tblView?app=ExoTbls&config=cumulative
- **File:** `df_processed.csv` - Processed dataset with features like equilibrium temperature, planetary radius, and habitability predictions.

## Analysis
- **Tools:** Python (Google Colab)
- **Methodology:**
  - Data cleaning and exploratory data analysis (EDA) to understand exoplanet characteristics.
  - Feature engineering, including insolation ratio and log transformations of equilibrium temperature and planetary radius.
  - Development of a logistic regression model to predict habitability, defined as planets with equilibrium temperatures between 200–400 K and planetary radii between 0.5–2 Earth radii.
- **Key Findings:**
  - The model identifies [X%] of exoplanets as potentially habitable based on the defined criteria.
  - Most exoplanets are classified as non-habitable, with a small cluster in the habitable zone (200–400 K, 0.5–2 Earth radii).
  - Visualization shows a clear decision boundary aligning with astrophysical expectations.

## Model Details
- **Type:** Logistic Regression (supervised machine learning)
- **Purpose:** Predicts the probability of an exoplanet being habitable based on equilibrium temperature (`koi_teq`) and planetary radius (`koi_prad`).
- **Features Used:** `koi_teq`, `koi_prad`, `koi_steff`, `koi_srad`, `insol_ratio`, `log_teq`, `log_prad`.
- **Evaluation:** Achieved an accuracy of [insert accuracy from your model, e.g., 0.85] on the test set, with a confusion matrix highlighting true/false positives and negatives.
- **Visualization:** A scatter plot with a probability contour illustrates the model’s decision boundary, available in the Colab notebook.
