Welcome!

This project was carried out in an academic setting as part of the coursework for the Business Analytics degree program at UCEMA (Buenos Aires).


### 1. Objective of the Analysis

The purpose of this project was to develop a predictive credit risk model based on a dataset provided by an international bank operating in Argentina. The aim was to understand which factors are associated with customer default and to build a model capable of anticipating such behavior, thus facilitating more informed credit decision-making.

---

### 2. Workflow

#### a. Data Cleaning and Preparation

- Irrelevant columns were removed from the analysis (`Unnamed: 0` and `indicador_aleatorio`).
- Missing values were identified and handled, especially in residential location variables (`residencial_Rural`, `residencial_Suburbana`, `residencial_Urbana`).
- Inconsistencies in data types were corrected: for example, the customer's age was initially in float format and was converted to integer.
- Categorical columns with different semantic representations were normalized (e.g., `"male"`, `"Hombre"` → `"male"`).
- Consistency checks were performed in relation to the declared geographic context (Argentina), as locations such as “Quito” and “Switzerland” appeared, which do not match the expected context.

#### b. Exploratory Analysis

- Unique values were segmented based on the target variable (`default`) to identify potential patterns.
- Differences were explored in variables such as `account_type`, `employment_status`, `product_level`, and `joint_account` to identify potential correlations with default behavior.

#### c. Predictive Modeling

- A classification model was built using a Decision Tree (`DecisionTreeClassifier`).
- The dataset was split into training and test sets, with cross-validation applied to ensure robustness.
- Evaluation metrics such as accuracy, precision, recall, and the confusion matrix were computed to assess model performance.

---

### 3. Results and Findings

- The model was able to reasonably predict default cases, although there is room for improvement using more complex models (e.g., Random Forest or XGBoost).
- Variables with strong predictive power were identified, such as `account type`, `employment status`, `customer age`, and `loan amount`.
- Some data inconsistencies (such as mislabeled categories or entries outside the declared geographic context) could be affecting model quality. These should be corrected in a future iteration.
- Descriptive analysis helped detect biases and better understand customer behavior based on different characteristics.

---

### 4. Conclusions

This analysis allowed:

- Identifying behavioral patterns associated with credit risk.
- Building a first version of a model that could be used to assist the bank in its credit granting decisions.
- Detecting opportunities for improvement both in data quality and in the choice of classification algorithm.
- Laying the foundation for a more robust risk management approach, combining data analysis with statistical and machine learning tools.
