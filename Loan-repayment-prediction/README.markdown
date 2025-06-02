# Loan Repayment Prediction

This project aims to predict whether a loan from the Lending Club dataset will be repaid (`loan_repaid`) using different models. We address class imbalance using Easy Enseble, Easy Enseble voting , SMOTE, evaluate multiple models, and optimize performance with metrics like ROC-AUC, precision, recall, and F1-score.

## Introduction

This project classifies loans as **repaid (1)** or **not repaid (0)** based on borrower and loan characteristics. We explore various machine learning models, preprocess the data to handle class imbalance, and evaluate performance using confusion matrices, classification reports, and ROC-AUC scores. The model is selected based on optimized thresholds to balance precision and recall.

## Dataset
The dataset used in this project was sourced from a Udemy course titled "Python for Data Science and Machine Learning Bootcamp".
It is based on Lending Club's loan data and has been specifically tailored by the course instructor to help students practice exploratory data analysis (EDA) and build real-world machine learning pipelines.

*Note*: To access the dataset, you can enroll in the course on Udemy. The dataset is provided as part of the course resources.

- **Source**: *https://www.udemy.com/course/python-for-data-science-and-machine-learning-bootcamp/?couponCode=ACCAGE0923* .You can enroll in the course to access the dataset.
- **Columns**:
- There are many LendingClub data sets on Kaggle. Here is the information on this particular data set:

LoanStatNew	                               Description
0	**loan_amnt**	  - The listed amount of the loan applied for by the borrower. If at some point in time, the credit department reduces the loan amount,                            then it will be reflected in this value.
1	**term**	      - The number of payments on the loan. Values are in months and can be either 36 or 60.
2	**int_rate**	  - Interest Rate on the loan
3	**installment**	  - The monthly payment owed by the borrower if the loan originates.
4	**grade**	      - LC assigned loan grade
5	**sub_grade**	  - LC assigned loan subgrade
6	**emp_title**	  - The job title supplied by the Borrower when applying for the loan.*
7	**emp_length**	  - Employment length in years. Possible values are between 0 and 10 where 0 means less than one year and 10 means ten or more years.
8	**home_ownership**- The home ownership status provided by the borrower during registration or obtained from the credit report. Our values are: RENT, OWN,                          MORTGAGE, OTHER
9	**annual_inc**	  - The self-reported annual income provided by the borrower during registration.
10	**verification_status**-Indicates if income was verified by LC, not verified, or if the income source was verified
11	**issue_d**	      - The month which the loan was funded
12	**loan_status**	  - Current status of the loan
13	**purpose**	      - A category provided by the borrower for the loan request.
14	**title**	      - The loan title provided by the borrower
15	**zip_code**	  - The first 3 numbers of the zip code provided by the borrower in the loan application.
16	**addr_state**	  - The state provided by the borrower in the loan application
17	**dti**	          - A ratio calculated using the borrower’s total monthly debt payments on the total debt obligations, excluding mortgage and the                                  requested LC loan, divided by the borrower’s self-reported monthly income.
18	**earliest_cr_line**-The month the borrower's earliest reported credit line was opened
19	**open_acc**	  - The number of open credit lines in the borrower's credit file.
20	**pub_rec**	      - Number of derogatory public records
21	**revol_bal**	  - Total credit revolving balance
22	**revol_util**	  - Revolving line utilization rate, or the amount of credit the borrower is using relative to all available revolving credit.
23	**total_acc**	  - The total number of credit lines currently in the borrower's credit file
24	**initial_list_status**-The initial listing status of the loan. Possible values are – W, F
25	**application_type**-Indicates whether the loan is an individual application or a joint application with two co-borrowers
26	**mort_acc**	  - Number of mortgage accounts.
27	**pub_rec_bankruptcies**-Number of public record bankruptcies

- **Class Imbalance**: ~80.4% Fully Paid (class 1), ~19.6% Charged Off (class 0).

## Technologies Used

- **Python Libraries**:
  - `numpy`, `pandas`: Data manipulation.
  - `matplotlib`, `seaborn`: Data visualization.
  - `scikit-learn`: Machine learning models (Logistic Regression, Random Forest, etc.) and metrics.
  - `imbalanced-learn`: SMOTE for handling class imbalance.
  - `tensorflow`, `keras`: Neural network models.
  - `xgboost`: Gradient boosting (optional).
- **Jupyter Notebook**: For developing and running the machine learning pipeline.

## Main Files:
- `EDA.ipynb`: Data cleaning and feature engineering
- `Utils.py`: Scalable modular functions
- `main.ipynb`: Full pipeline using SMOTE + ensemble models
- `Requirment.txt`: all Libraries 

## Models Used:
- `Logistic Regression`
- `Random Forest`
- `XGBoost`
- `Naive Bayes`
- `Deep Neural Network (Keras)`

## Add-ons:
- `Easy Ensemble`
- `SMOTE Resampling`
- `MinMax Scaling`
- `Voting Ensemble`
- `Threshold Optimization`
- `ROC & PR Curve Analysis`
  
## Steps Involved
### Step 1: Data Processing
- Cleaning, encoding, and feature engineering in `EDA.ipynb`
- Save cleaned data as `cleaned_data.pkl`

### Step 2: Modular Utilities
- Located in `Utils.py`
- Functions for:
  - Scaling
  - Model training
  - SMOTE resampling
  - Neural Network creation & training
  - Ensemble modeling (Random Forest, Logistic, XGBoost, DNN)
  - Evaluation: ROC-AUC, PR curve, F1 optimization
  - Ensemble Voting

### Step 3: Execution in `main.ipynb`
- Load cleaned data
- Apply SMOTE and scaling
- Train models & ensembles
- Evaluate performance with threshold optimization
- Visualize ROC & PR curves

---

## Model Performance

Each model is evaluated using:
-**Confusion matrics** - A summary of prediction results
- **Precision** – Accuracy of positive (repaid) predictions
- **Recall** – Correctly found repaid loans
- **F1-Score** – Balance between precision and recall
- **ROC-AUC** – Area under the ROC curve

----
## How to Run the Project

# Run Locally (Jupyter Notebook)

1. **Clone the Repository**
   ```bash
   git clone https://github.com/Surajit-maity110/Loan-repayment-prediction.git
   cd Loan-repayment-prediction

2. **Install Dependencies** - pip install -r requirements.txt

3. Run the Jupyter Notebook - jupyter notebook main.ipynb

4. Dataset Access (Important)
**"Python for Data Science and Machine Learning Bootcamp"**  
[Course Link] - *https://www.udemy.com/course/python-for-data-science-and-machine-learning-bootcamp/?couponCode=ACCAGE0923*
i.Make sure you’ve downloaded the Lending Club dataset from the Udemy course

ii.Run EDA.ipynb to clean and save cleaned_data.pkl

iii.Confirm cleaned_data.pkl is in the project directory

----

## Contributing

Want to contribute to this project? Here’s how you can do it step by step:

**Fork the Repository**
Click the Fork button on the top-right of this GitHub repo to create a copy under your own GitHub account.

**Clone the Fork**
Download your forked project to your local machine.

**Create a New Branch**
Make a new branch where you'll write your changes. This keeps the main project stable.

**Make Your Changes**
Add or improve code, fix bugs, enhance documentation, or try new features.

**Commit and Push**
Save your changes and push them to your branch on GitHub.

**Create a Pull Request**
Go to your GitHub fork and click “Compare & pull request”. Add a clear title and description, then submit.

---

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.