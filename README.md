# Heart Disease Analysis and Prediction

This workflow demonstrates data exploration, visualization, and classification model training for **heart disease** prediction. Below is an outline of the steps taken:

---

## 1. Data Loading and Inspection
1. **Load the dataset**: A CSV file named `heart.csv` is read into a pandas DataFrame.  
2. **Initial exploration**: Display the first few rows (`head()`), view descriptive statistics (`describe()`), and confirm there are no missing values (`isnull().values.any()`).
3. **Basic checks**: Investigate the distribution of specific features (e.g., `sex`).

---

## 2. Exploratory Data Analysis (EDA)
1. **Subset the data**: Separate records for patients with heart disease (`output == 1`) and those without (`output == 0`).
2. **Histograms**: Plot the distribution of features like `age` and `thalachh` (max heart rate) for each group.
3. **Boxplots**: Compare the distributions of numeric features (e.g., `thalachh`) between the two groups via boxplots.
4. **Correlation**: Generate a correlation matrix to identify relationships between variables. Visualize it using heatmaps (e.g., Seaborn, Plotly).

---

## 3. Visualizations
1. **Seaborn plots**: 
   - Violin plots, pairplots, strip plots to understand data patterns and potential class separability.  
2. **Plotly**:
   - Interactive histograms and boxplots (e.g., for `output`, colored by `sex`) provide insights into how different demographics relate to heart disease.
   - Boxplots for features like `age`, `thalachh`, and `trtbps` grouped by `output`.

---

## 4. Data Preprocessing
1. **Information check**: Review data types and non-null counts (`df.info()`).
2. **Splitting**:
   - Assign the target variable (`output`) to `y` and the remaining columns to `X`.
   - Perform a train–test split (e.g., 80/20) to separate the dataset for training and validation.
3. **Scaling**:
   - Use a standard scaler (`StandardScaler`) to normalize numeric features in both training and test sets.

---

## 5. Model Training
1. **Define classifiers**:
   - Logistic Regression  
   - Decision Tree  
   - Random Forest  
   - K-Nearest Neighbors  
   - Support Vector Classifier  
   - XGBoost  
2. **Fitting**: Train each model on the scaled training data.
3. **Predictions**: Generate predictions on the test set.
4. **Evaluation**: Calculate accuracy scores (`accuracy_score`) to compare performance across models.

---

## 6. Hyperparameter Tuning
1. **Parameter grid**: Define candidate hyperparameters (e.g., `n_neighbors`, `weights`, `metric` for KNN).
2. **GridSearchCV**: Perform a grid or randomized search across these parameters to find the best combination.
3. **Refit model**: Using the best parameters, retrain and evaluate on the test set to check for improvements.

---

## 7. Results and Observations
1. **Accuracy comparison**: Identify the top-performing classifiers for heart disease prediction.
2. **Visual insights**: From EDA plots, note key differentiating features (e.g., `thalachh` and `age` across different `output` groups).
3. **Refinement**: Use hyperparameter tuning results to optimize models like KNN for better performance.

---

## License
This project is open-source. You are free to use, modify, and distribute the code. If you use it in your own work, a reference or link back to this repository is appreciated.

---

Feel free to adapt this single-notebook guide to your preferences or add deeper domain-specific analysis.
