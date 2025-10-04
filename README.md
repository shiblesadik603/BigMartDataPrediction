# BigMart Data Prediction

This project leverages machine learning techniques to predict the sales of products at various outlets of BigMart. The analysis covers data cleaning, exploratory data analysis (EDA), feature engineering, and model training, culminating in a regression model to forecast `Item_Outlet_Sales`.

## Dataset

The dataset contains historical sales data for BigMart and includes the following features:

- `Item_Identifier`: Unique ID for each product
- `Item_Weight`: Weight of the product
- `Item_Fat_Content`: Whether the product is low fat or regular
- `Item_Visibility`: Percentage of total display area of all products in a store allocated to the particular product
- `Item_Type`: Category to which the product belongs
- `Item_MRP`: Maximum Retail Price (list price) of the product
- `Outlet_Identifier`: Unique store ID
- `Outlet_Establishment_Year`: Year in which store was established
- `Outlet_Size`: Size of the store
- `Outlet_Location_Type`: Store location
- `Outlet_Type`: Type of store
- `Item_Outlet_Sales`: Sales of the product at the particular store (target variable)

## Project Workflow

1. **Data Loading & Inspection**  
   Load the dataset, inspect the first few rows, and check for missing values.

2. **Data Cleaning**  
   - Fill missing values in `Item_Weight` with the mean.
   - Fill missing values in `Outlet_Size` with the mode based on `Outlet_Type`.
   - Standardize categorical values (e.g., unify different representations of `Item_Fat_Content`).

3. **Exploratory Data Analysis (EDA)**  
   - Visualize distributions of numeric and categorical columns using `matplotlib` and `seaborn`.
   - Analyze correlations and feature distributions to gain insights.

4. **Feature Engineering**  
   - Encode categorical variables using `LabelEncoder`.

5. **Model Building**  
   - Split the data into train and test sets.
   - Train an `XGBRegressor` to predict `Item_Outlet_Sales`.
   - Evaluate the model using appropriate metrics.

## Requirements

- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- xgboost

You can install the requirements using:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost
```

## Usage

1. Clone the repository and navigate to the project directory.
2. Ensure that the dataset `big_mart_data.csv` is present in the same directory as the notebook.
3. Open and run `BigMartDataPrediction.ipynb` in Jupyter Notebook or any compatible environment.

## Notebooks

- **BigMartDataPrediction.ipynb**: Main notebook containing the complete workflow from data cleaning to model evaluation.

## Results

- The notebook demonstrates step-by-step preprocessing, EDA, encoding, and regression modeling.
- Visualizations provide insights into the data distribution and relationships between features.

## Acknowledgements

- Dataset and problem inspiration: [BigMart Sales Prediction](https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/)

---

**Author**: [shiblesadik603](https://github.com/shiblesadik603)
