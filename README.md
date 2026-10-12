# MLTrackPro: Reproducible Machine Learning Experiments

## Overview

MLTrackPro is a machine learning project that demonstrates experiment
tracking using MLflow and dataset/model versioning using DVC.

The project compares three machine learning models on the
Breast Cancer Wisconsin dataset.

## Technologies Used

- Python
- Scikit-learn
- Pandas
- MLflow
- DVC
- Jupyter Notebook
- Git and GitHub

## Machine Learning Models

1. Logistic Regression
2. Random Forest
3. Support Vector Machine (SVM)

## Experiment Results

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---:|---:|---:|---:|
| Logistic Regression | 98.25% | 98.61% | 98.61% | 98.61% |
| Random Forest | 95.61% | 95.89% | 97.22% | 96.55% |
| SVM | 98.25% | 98.61% | 98.61% | 98.61% |

## MLflow

MLflow records the parameters, evaluation metrics, and model artifacts
for each training experiment.

To start the MLflow UI, run:

```bash
python -m mlflow ui --backend-store-uri sqlite:///mlflow.db
```

Open http://127.0.0.1:5000 in your browser.

## DVC

DVC tracks the dataset and trained model files.

Tracked files:

- `data/dataset.csv.dvc`
- `models.dvc`

Push the dataset and models to the configured DVC remote:

```bash
dvc push
```

Restore the dataset and models:

```bash
dvc pull
```

**Note:** The current DVC remote is a local folder. Shared storage is
needed to reproduce the project on another computer.

## Project Structure

```text
MLTrackPro/
├── data/
│   ├── dataset.csv.dvc
│   └── .gitignore
├── models.dvc
├── experiment_tracking.ipynb
├── screenshots/
│   └── run.png
├── .dvc/
├── .dvcignore
├── .gitignore
└── README.md
```

## How to Run

1. Clone the GitHub repository.
2. Install the required Python libraries.
3. Configure access to the DVC remote.
4. Retrieve the dataset and models using `dvc pull`.
5. Open `experiment_tracking.ipynb` in Jupyter Notebook.
6. Run the notebook cells to reproduce the experiments.

## GitHub Repository

https://github.com/student-Madhumitakhatua/MLTrackPro

## Disclaimer

This project is an educational machine learning demonstration.
It is not intended for medical diagnosis or clinical decision-making.