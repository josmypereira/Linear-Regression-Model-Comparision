# 📊 Linear Regression with Python: Model Comparison

## Project Overview
This project aims to compare multiple regression techniques to find the best model for predicting house prices using the `house_data` dataset. This dataset includes various features, such as house characteristics, location, and amenities. Three regression models were used and evaluated:

1. **Linear Regression**
2. **Polynomial Regression** (degree = 2)
3. **Random Forest Regressor**

By analyzing and comparing the models, we determined the most suitable model for accurately predicting house prices.

---

## 📋 Data Description
The dataset contains 21 features, including:
- **2 categorical variables**
- **17 continuous variables**
- **House ID** and **Date sold**

### Sample Data Structure
| Variable Name   | Description                        | Sample Data |
| --------------- | ---------------------------------- | ----------- |
| Id              | House ID                           | 7129300520; ...|
| date            | Date house sold                    | 20141013T000000; 20141209T000000; ...|
| price           | House price                        | 221900; 538000; ... |
| bedrooms        | Number of bedrooms                 | 3; 2; ... |
| bathrooms       | Number of bathrooms                | 1; 2.25; ... |
| sqft_living     | Living room size (in sqft)         | 1180; 2570 |
| waterfront      | Access to waterway (0 = no, 1 = yes)| 0; 1; ... |

---

## 🔍 Exploratory Data Analysis (EDA)
The EDA included:
1. **Correlation Analysis**: Used a heatmap to find highly correlated features.
2. **Feature Visualization**: Visualized the effect of various features on house prices (e.g., bathrooms, bedrooms).
3. **Outlier Detection**: Detected and assessed outliers that could impact model performance.

## ⚙️ Data Preprocessing
- **Dropped Irrelevant Columns**: Removed ID and target (`price`) from the feature set.
- **Date Transformation**: Transformed the `date` column into `year`, `month`, and `day`.
- **Train-Test Split**: Split the data into training (80%) and testing (20%) sets.
- **Feature Scaling**: Applied scaling to optimize model performance.

---

## 🚀 Model Training and Evaluation
Three models were trained, each evaluated based on Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and R-Squared.

### Model 1: Linear Regression
- A standard Linear Regression model was trained with continuous features.
- Evaluated on MSE, RMSE, and R-Squared values.

### Model 2: Polynomial Regression (Degree = 2)
- Transformed the features using PolynomialFeatures with degree = 2.
- Trained with Linear Regression and evaluated similarly.

### Model 3: Random Forest Regressor
- Utilized a Random Forest Regressor with 1000 estimators.
- Compared using the same evaluation metrics.

---

## 📊 Results Comparison
| Model                  | MAE     | MSE     | RMSE    | R-Squared |
| ---------------------- | ------- | ------- | ------- | --------- |
| **Linear Regression**  | 126929.173470    | 4.495149e+10    | 212017.668945    | 0.702656      |
| **Polynomial Regression (Degree 2)** | 104067.660103 | 3.019502e+10 | 173767.131391 | 0.800267    |
| **Random Forest Regressor** | 72522.055112 | 2.147901e+10  | 146557.191274    | 0.857921      |

- **Best Model**: Based on the above metrics, **Random Forest Regressor** yielded the lowest error and highest R-Squared value.

## 📈 Visual Analysis
The model predictions were plotted against true values to visually inspect performance and potential overfitting.

---

## 🛠️ Libraries and Tools
- **Python Libraries**: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`
- **Visualization Tools**: `hvplot`

