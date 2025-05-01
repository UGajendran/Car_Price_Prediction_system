# 🚗 Car Price Prediction Model

This project provides a clean and straightforward implementation of a machine learning model that predicts car prices based on features from a structured dataset. The model is built using **Linear Regression** and includes basic data cleaning, preprocessing, and model evaluation.

## 📁 Files

- `car_price_model.ipynb` – Jupyter Notebook containing the entire workflow: loading data, preprocessing, training the model, and evaluating it.
- `Cardetails.csv` – The dataset containing various details about cars, used for training the model.

---

## 📊 Dataset Overview

The dataset contains the following columns:

- `name` — Full name of the car (including brand and model)
- `year` — Manufacturing year
- `km_driven` — Kilometers the car has been driven
- `fuel` — Type of fuel used (e.g., Petrol, Diesel)
- `seller_type` — Type of seller (e.g., Individual, Dealer)
- `transmission` — Transmission type (Manual/Automatic)
- `owner` — Ownership status (e.g., First owner, Second owner)
- `mileage`, `engine`, `max_power`, `seats` — Vehicle specifications
- `selling_price` — Target variable (price of the car)
- `torque` — Removed during preprocessing due to inconsistency

---

## 🧹 Data Cleaning and Preprocessing

The following steps were performed:

1. **Column Removal**:
   - Dropped the `torque` column due to inconsistent formatting.
  
2. **Missing Values**:
   - Removed all rows with missing values using `dropna()`.
  
3. **Duplicates**:
   - Checked for and removed duplicate rows.
  
4. **Feature Engineering**:
   - Extracted the car brand from the `name` column using string splitting.
   - Cleaned columns like `mileage`, `engine`, and `max_power` to retain only numeric values.

---

## 🤖 Model Development

- **Algorithm**: Linear Regression (`sklearn.linear_model.LinearRegression`)
- **Input Features**: Selected numerical and categorical features after cleaning.
- **Target Variable**: `selling_price`
- **Train-Test Split**: 80% training and 20% testing using `train_test_split`

---

## 📈 Evaluation

- The model was trained and predictions were generated on the test set.
- Basic model metrics and comparisons between actual and predicted prices were displayed using printed outputs (no graphical evaluation used).

---

## 🛠️ Dependencies

Make sure you have the following Python libraries installed:

```bash
pandas
numpy
scikit-learn
```

---

## 🚀 How to Run

1. Clone the repository or download the files.
2. Open `car_price_model.ipynb` in Jupyter Notebook or Google Colab.
3. Ensure `Cardetails.csv` is in the same directory or update the file path in the notebook.
4. Run all cells sequentially to:
   - Load and inspect the dataset
   - Preprocess and clean the data
   - Train the Linear Regression model
   - Evaluate performance
