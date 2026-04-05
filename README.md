# Robust-SAR-Prediction-Program-in-R
Pro SAR Prediction
# 🧪 Java-Free SAR Prediction Platform
A fully local, highly scalable Structure-Activity Relationship (SAR) prediction engine built entirely in R. 

## Overview
Traditional cheminformatics pipelines often rely on heavy Java dependencies (like `rJava` and `rcdk`) to compute molecular fingerprints, causing massive environment headaches. This platform solves that by utilizing a custom, purely vectorized R descriptor engine to extract 60 2D pharmacophores and molecular properties directly from SMILES strings. 

It is designed for rapid, high-throughput triage of small molecule libraries and PROTAC candidates using Machine Learning (XGBoost/Random Forest).

## Features
* **Zero Java Required:** Runs flawlessly on any OS without `rJava` path errors.
* **Massively Scalable:** Vectorized `stringr` operations process thousands of SMILES in seconds.
* **Advanced ML Backend:** Features automated hyperparameter tuning for XGBoost and Random Forest models via the `caret` ensemble.
* **Interactive UI:** Built with Shiny for a seamless, code-free user experience.

## How to Use (For Non-Coders)
You do not need to install R or know how to code to use this tool!
1. Click the live web link above.
2. Download the `sar_test_data.csv` file from the `data/` folder in this repository.
3. Upload it to the application, select **XGBoost**, and click **Train**.
4. Paste a new SMILES string (e.g., Aspirin: `CC(=O)OC1=CC=CC=C1C(=O)O`) into the prediction box to see the results.

## How to Run Locally (For Developers)
If you want to run the code on your own machine:
1. Clone this repository.
2. Open `SAR.R` in RStudio.
3. Run the script. The built-in package manager will automatically install `shiny`, `xgboost`, `caret`, and other dependencies.
