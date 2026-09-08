# Telecom Customer Churn Prediction

## Project Overview

This project predicts whether a telecom customer is likely to churn or continue using the service.

The complete Machine Learning workflow includes data preprocessing, model training, evaluation, Streamlit application development, Docker containerization, CI/CD and AWS deployment.

## Business Problem

Customer churn is an important problem for telecom companies.

If a company can identify customers who are likely to leave, it can take retention actions such as better offers, support or personalized services.

The objective of this project is to predict:

* **No** - Customer is unlikely to churn
* **Yes** - Customer is likely to churn

## Dataset

The dataset contains:

* **7043 customer records**
* **21 columns**

Important features include:

* Gender
* SeniorCitizen
* Partner
* Dependents
* Tenure
* PhoneService
* InternetService
* OnlineSecurity
* TechSupport
* Contract
* PaymentMethod
* MonthlyCharges
* TotalCharges
* Churn

## Data Preprocessing

For numerical features:

* Missing values handled using `SimpleImputer`
* Median strategy used for missing values
* Scaling performed using `StandardScaler`

For categorical features:

* Missing values handled using `SimpleImputer`
* Most frequent strategy used
* Categorical features encoded using `OneHotEncoder`
* `handle_unknown="ignore"` used for unseen categories

A `ColumnTransformer` was used to combine numerical and categorical preprocessing.

## Machine Learning Model

The classification model used in this project is:

**Logistic Regression**

The preprocessing and Logistic Regression model were combined into a Machine Learning pipeline.

## Model Performance

### Accuracy

**80.55%**

### ROC-AUC Score

**0.842**

### Confusion Matrix

| Actual / Predicted |  No | Yes |
| ------------------ | --: | --: |
| No                 | 926 | 109 |
| Yes                | 165 | 209 |

### Classification Report

| Class    | Precision | Recall | F1 Score |
| -------- | --------: | -----: | -------: |
| No Churn |      0.85 |   0.89 |     0.87 |
| Churn    |      0.66 |   0.56 |     0.60 |

The model achieved good overall classification performance and an ROC-AUC score of approximately 0.84.

## Streamlit Application

A Streamlit web application was developed for real-time customer churn prediction.

The user can enter customer information and receive:

* Churn prediction
* Churn probability
* Real-time prediction result

Example:

**Prediction: Yes**

**Churn Probability: approximately 69%**

## Docker

The Machine Learning application was containerized using Docker.

Docker helps package the application, trained model and dependencies into a consistent environment.

## CI/CD

GitHub Actions was used to automate the project workflow.

The project includes:

* Continuous Integration
* Continuous Testing
* Continuous Deployment

## AWS Deployment

The application was deployed using AWS services.

Technologies used:

* Amazon ECR
* Amazon ECS
* AWS Fargate
* Docker
* GitHub Actions

The Docker image is stored in Amazon ECR and deployed using Amazon ECS.

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Logistic Regression
* Streamlit
* Docker
* Git
* GitHub
* GitHub Actions
* AWS ECR
* AWS ECS
* AWS Fargate

## Project Structure

```text
Telecom-Customer-Churn-ML/
│
├── app.py
├── churn_model.ipynb
├── churn_model.pkl
├── telcom_churndataset.csv
├── requirements.txt
├── Dockerfile
├── .dockerignore
├── README.md
│
└── .github/
    └── workflows/
```

## How to Run Locally

Clone the repository:

```bash
git clone https://github.com/Umesh1234AI-afk/Telecom-Customer-Churn-ML.git
```

Go to the project folder:

```bash
cd Telecom-Customer-Churn-ML
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the Streamlit application:

```bash
streamlit run app.py
```

## Key Learnings

This project helped me gain practical experience in:

* Data preprocessing
* Feature transformation
* Machine Learning pipelines
* Logistic Regression
* Model evaluation
* ROC-AUC analysis
* Streamlit application development
* Docker containerization
* GitHub Actions
* CI/CD
* AWS deployment

## Future Improvements

Future improvements may include:

* Random Forest
* XGBoost
* Hyperparameter tuning
* Class imbalance handling
* SHAP explainability
* Model monitoring
* Data drift detection
* FastAPI integration

## Author

**Umesh Chandra**

Data Science | Machine Learning | MLOps

GitHub: Umesh1234AI-afk
