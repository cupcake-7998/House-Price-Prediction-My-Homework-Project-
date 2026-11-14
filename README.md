# 🏡 California House Price Prediction | Machine Learning Project

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Machine%20Learning-Regression-orange" alt="Machine Learning: Regression" />
  <img src="https://img.shields.io/badge/Scikit--Learn-Models-F7931E?logo=scikitlearn&logoColor=white" alt="Scikit-learn" />
  <img src="https://img.shields.io/badge/Notebook-Google%20Colab%20%7C%20Jupyter-F37626?logo=jupyter&logoColor=white" alt="Jupyter Notebook" />
  <img src="https://img.shields.io/badge/Project-Educational-blue" alt="Educational project" />
</p>

<p align="center"><strong>Turning California housing data into data-driven price estimates.</strong></p>

---

## 📌 Project Overview

This project explores how machine learning regression models can estimate median house values across California. Using the California Housing dataset provided by Scikit-learn, the notebook walks through data exploration, preprocessing, model comparison, and evaluation.

It is an educational, notebook-based project designed to demonstrate a complete introductory regression workflow—not a production real-estate valuation service.

## 🎯 Project Objectives

- Explore housing data and understand its features.
- Visualize the target distribution and its relationship with median income.
- Build a reusable preprocessing and modeling pipeline.
- Compare multiple regression algorithms on a held-out test set.
- Evaluate predictions with MAE, RMSE, and R².

## ✨ Highlights

- Loads the California Housing dataset directly from Scikit-learn.
- Uses an 80/20 train-test split, stratified by target-price bins.
- Builds pipelines with median imputation and feature scaling.
- Compares Ridge Regression, Random Forest, and Histogram-based Gradient Boosting.
- Reports model results using common regression metrics.
- Includes exploratory charts and a permutation-importance analysis in the notebook.

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Programming language |
| Pandas and NumPy | Data handling and numerical operations |
| Matplotlib and Seaborn | Data visualization |
| Scikit-learn | Dataset loading, preprocessing, modeling, and evaluation |
| Jupyter Notebook / Google Colab | Interactive development |

## 📊 Dataset and Features

The notebook fetches `fetch_california_housing` from `sklearn.datasets`. The dataset contains 20,640 observations and eight input features:

| Feature | Description |
|---|---|
| `MedInc` | Median income in the block group |
| `HouseAge` | Median house age in the block group |
| `AveRooms` | Average rooms per household |
| `AveBedrms` | Average bedrooms per household |
| `Population` | Block group population |
| `AveOccup` | Average household occupancy |
| `Latitude` | Block group latitude |
| `Longitude` | Block group longitude |

The target is median house value. **Target values are measured in units of $100,000**; for example, `2.5` represents $250,000. The dataset is downloaded when the notebook runs, so an internet connection is required the first time.

## 🧠 Machine Learning Workflow

1. Load and inspect the California Housing dataset.
2. Review feature statistics and check for missing values.
3. Plot the target distribution and median income relationship.
4. Split the data into training and test sets (80/20), stratifying by target bins.
5. Apply median imputation and standard scaling in an Scikit-learn pipeline.
6. Train and compare Ridge, Random Forest, and HistGradientBoosting regressors.
7. Evaluate model predictions using MAE, RMSE, and R², and inspect feature importance.

## 📈 Model Comparison

The notebook's baseline model comparison reports the following test-set results:

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| HistGradientBoostingRegressor | 0.319966 | 0.478777 | 0.826301 |
| RandomForestRegressor | 0.369646 | 0.542755 | 0.776777 |
| Ridge Regression | 0.536416 | 0.742747 | 0.581964 |

Since the target is expressed in $100,000 units, the leading model's MAE of `0.319966` corresponds to approximately **$32,000** in median absolute error on this evaluation. These are notebook-reported results; rerunning the notebook may produce different results if code, library versions, or data change.

## 📂 Repository Structure

```text
House-Price-Prediction-My-Homework-Project-/
├── README.md
└── house_price_prediction.ipynb
```

The notebook writes a local `pipeline.py` helper during execution; it is generated in the runtime and is not currently a separate repository file.

## 🚀 Getting Started

### Option 1: Google Colab

Open [`house_price_prediction.ipynb`](https://colab.research.google.com/github/cupcake-7998/House-Price-Prediction-My-Homework-Project-/blob/main/house_price_prediction.ipynb) in Google Colab and run the cells in order. The notebook installs its required packages and downloads the dataset when executed.

### Option 2: Run locally

Clone this repository and install the notebook dependencies:

```bash
git clone https://github.com/cupcake-7998/House-Price-Prediction-My-Homework-Project-.git
cd House-Price-Prediction-My-Homework-Project-
pip install scikit-learn pandas numpy matplotlib seaborn joblib jupyter
jupyter notebook
```

Open `house_price_prediction.ipynb` and run the cells sequentially. An internet connection is needed to fetch the dataset.

## 💡 What This Project Demonstrates

- Exploratory analysis of a real-world tabular dataset.
- Use of Scikit-learn pipelines to combine preprocessing and modeling.
- Comparison of linear and tree-based regression models.
- Evaluation with MAE, RMSE, and R².
- Reproducible experimentation with a fixed random seed.

## 🔮 Possible Next Steps

- Add a `requirements.txt` file with pinned dependency versions.
- Move reusable preprocessing and model code into tracked Python modules.
- Add automated tests and a repeatable training script.
- Publish visualizations and document tuned-model results separately.
- Build a small interactive demo for exploring predictions.

## 👨‍💻 Author

**Shivaram** — [GitHub profile](https://github.com/cupcake-7998)

---

⭐ If you find this educational project useful, consider giving the repository a star.

<p align="center"><em>Built with Python, machine learning, and curiosity. 🚀</em></p>
