# Iris ML App

A Streamlit app that explores the Iris dataset and compares five classic classifiers.

![Streamlit app](Streamlit%20photo.png)

## What it does

The app predicts the iris species (setosa, versicolor or virginica) from four flower measurements: sepal length, sepal width, petal length and petal width. The dataset has 150 flowers, 50 per species. You can explore the data with charts and then train five models and compare their accuracy.

## How it works

The sidebar has four sections:

1. **EDA** – summary statistics, class counts, pair plots, a 3D scatter plot and a correlation heatmap.
2. **Algorithms** – trains one model at a time with 10-fold cross-validation and shows its mean accuracy:
   - K-nearest neighbors (choose K with a slider)
   - Gaussian Naive Bayes
   - Support vector classifier (choose C)
   - Logistic regression
   - Decision tree (choose max depth)
3. **Results** – accuracy of each model and a box plot comparing them.
4. **About** – short description of the project.

## Quick start

1. Download `Iris.csv` (Kaggle "Iris Species" dataset, with an `Id` column) and put it in `dataset_/Iris.csv`.
2. Install and run:

```bash
pip install -r requirements.txt
streamlit run main.py
```

## Project structure

```
main.py            The Streamlit app
requirements.txt   Pinned package versions (2020)
versicolor.jpg     Image shown at the top of the app
Streamlit photo.png  Screenshot for this README
```

## Notes and limitations

- This was a university learning project from 2022.
- The dataset is not included in the repo.
- The pinned versions are old (Streamlit 0.71, scikit-learn 0.23). They need an older Python, around 3.8. The `sklearn==0.0` line no longer installs with current pip. Remove it if you use a newer setup.
- The Results section expects all five models to have been run first in the Algorithms section.
