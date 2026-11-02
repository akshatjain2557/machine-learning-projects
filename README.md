# Machine Learning Projects

A collection of three Jupyter notebooks demonstrating regression and classification with scikit-learn. Each notebook contains its own data preparation, model training, evaluation, and visualizations.

## Projects

| Project | Dataset | Algorithm | Reported results |
|---|---|---|---|
| [Car price prediction](notebooks/car-price-multiple-linear-regression.ipynb) | `car data.csv` (301 used-car listings). Predicts `Selling_Price` from year, present price, kilometers driven, fuel type, seller type, transmission, and owner count. | Multiple linear regression in a scikit-learn pipeline, with one-hot encoding for categorical inputs; 80/20 train/test split (`random_state=42`). | MAE: **1.2162**; RMSE: **1.8652**; R²: **0.8490**. |
| [Salary prediction](notebooks/salary-simple-linear-regression.ipynb) | `Salary_dataset.csv` (30 observations). Predicts `Salary` from `YearsExperience`. | Simple linear regression; 80/20 train/test split (`random_state=42`). | MAE: **6,286.45**; RMSE: **7,059.04**; R²: **0.9024**. The fitted slope is about **9,423.82** salary units per experience year. |
| [Telco customer churn](notebooks/telco-customer-churn-logistic-regression.ipynb) | `WA_Fn-UseC_-Telco-Customer-Churn.csv` (7,043 customer records; 7,032 remain after numeric conversion and dropping missing `TotalCharges`). Predicts whether a customer churns. | Logistic regression (`max_iter=1000`), one-hot encoded features, standardized inputs, and stratified 80/20 train/test split (`random_state=42`). | Accuracy: **0.8038** on 1,407 test records. Confusion matrix (actual rows `[stay, churn]`, predicted columns `[stay, churn]`): `[[916, 117], [159, 215]]`. Churn-class precision: **0.65**, recall: **0.57**, F1: **0.61**. |

Metrics above are the outputs saved in the supplied notebooks and describe their recorded train/test runs. They are included as reported, without rerunning or changing the notebooks.

## Data and running the notebooks

The notebooks expect their CSV datasets in the notebook's working directory. The CSV files were not part of the supplied files and are not included here. Place the corresponding dataset beside a notebook before running it, then open the notebook in Jupyter with the Python 3 kernel and install its imports (`pandas`, `numpy`, `matplotlib`, `seaborn`, and `scikit-learn` as needed).

## Repository layout

```text
.
├── README.md
└── notebooks/
    ├── car-price-multiple-linear-regression.ipynb
    ├── salary-simple-linear-regression.ipynb
    └── telco-customer-churn-logistic-regression.ipynb
```
