# 🏠 Boston Housing Price Prediction

This project uses regression models to predict housing prices in Boston based on several real estate features. The goal is to understand how different features (like crime rate, number of rooms, etc.) affect house prices, and to build models that can make accurate predictions.

---

## 📁 Dataset

The dataset is a cleaned version of the classic Boston Housing dataset, and includes the following features:

| Feature     | Description |
|-------------|-------------|
| CRIM        | Crime rate per capita |
| ZN          | Residential land zoned for large lots |
| INDUS       | Non-retail business acres per town |
| CHAS        | Charles River (1 if tract bounds river, 0 otherwise) |
| NOX         | Nitric oxide concentration |
| RM          | Average number of rooms per dwelling |
| AGE         | Percentage of owner-occupied units built before 1940 |
| DIS         | Distance to employment centers |
| RAD         | Index of accessibility to radial highways |
| TAX         | Property tax rate |
| PTRATIO     | Pupil-teacher ratio |
| B           | Proportion of Black residents |
| LSTAT       | % lower status of the population |
| **MEDV**    | Median home value (Target variable) |

---

## 🔍 Models Applied

### 🔹 1. Simple Linear Regression
- A basic regression using one feature (e.g., `RM` or `LSTAT`) to predict `MEDV`.
- Helps visualize the linear relationship between a single feature and house prices.

### 🔹 2. Multiple Linear Regression
- Uses **all numerical features** to predict `MEDV`.
- This model can better capture the influence of multiple factors on house pricing.
- Model is trained on a normalized dataset to ensure fair comparison across features.

### 🔹 3. Polynomial Regression
- Extends linear regression by including **non-linear (squared/cubic)** terms.
- Captures more complex patterns in the data (e.g., price curves that bend).
- Degree-4 polynomial often provides a good balance between accuracy and overfitting.

---

## ⚙️ Steps Performed

1. Data Loading and Exploration (`boston.csv`)
2. Preprocessing (e.g., scaling, train-test split)
3. Fitting:
   - Simple linear model
   - Full multiple regression
   - Polynomial regression (degree 2)
4. Evaluation using **Mean Squared Error (MSE)**
5. Visualizations of predictions vs. actual values

---

## 📉 Evaluation Metric

- The main metric used is **MSE (Mean Squared Error)**.
- Lower MSE indicates better prediction performance.

---

## 💻 How to Run

1. Clone this repository or download the notebook.
2. Install required libraries:
   ```bash
   pip install pandas scikit-learn matplotlib

Linear Regression MSE:            ~4.6769
Multiple Linear Regression MSE:   ~17.23
Polynomial Regression MSE:        ~6.1711
