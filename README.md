# House Price Prediction Using Regression

## Project Overview

This project focuses on predicting house prices using regression techniques and property-related features. It includes data cleaning, exploratory data analysis (EDA), feature preparation, model training, and evaluation.

## Dataset

- **File:** `houseprice.csv.csv`
- **Initial records:** 3,479
- **Columns:** 8
- **Target variable:** `Price`
- **Input features:** 5

The dataset contains property information such as:
- Area
- Number of rooms
- Parking availability
- Warehouse availability
- Elevator availability
- Address
- Price
- Price in USD

The `Price` column was used as the prediction target. The `Address` and `Price(USD)` columns were not included in the model features.

## Data Preprocessing

The following preprocessing steps were performed:

1. Removed records with missing addresses.
2. Converted the `Area` column to numeric values.
3. Removed records with invalid or missing area values.
4. Detected and removed area outliers using the Interquartile Range (IQR) method.
5. Encoded binary property features:
   - Parking
   - Warehouse
   - Elevator
6. Split the data into training and testing sets (80/20).
7. Applied `StandardScaler` to the input features, fitting the scaler only on the training data.

After cleaning, the dataset contained **3,219 records**.

## Exploratory Data Analysis

Exploratory analysis included:
- Examining the distribution of property areas before and after cleaning.
- Visualizing the area distribution using histograms and KDE.
- Reviewing the dataset before and after preprocessing.

## Model

The notebook implements a **Linear Regression** model using the following input features:

- Area
- Room
- Parking
- Warehouse
- Elevator

## Model Evaluation

The Linear Regression model was evaluated using MAE, RMSE, and R².

| Metric | Result |
|---|---:|
| MAE | 1,828,332,092.32 |
| RMSE | 2,658,098,893.54 |
| R² Score | 0.5543 |

The MAE and RMSE are expressed in the same unit as the target variable (`Price`). The model achieved an R² score of approximately 0.55 on the held-out test set.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Repository Structure

```text
house-price-prediction/
│
├── regression.ipynb
├── houseprice.csv.csv
└── README.md
```

## How to Run

1. Clone this repository.
2. Install the required Python libraries.
3. Place `houseprice.csv.csv` in the same directory as the notebook.
4. Open `regression.ipynb` using Jupyter Notebook or Google Colab.
5. Run the notebook cells in order.

## Disclaimer

This project is an educational machine learning exercise. Its predictions are based on the available dataset and selected features and should not be treated as professional property valuations.
