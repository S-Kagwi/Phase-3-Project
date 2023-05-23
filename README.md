# SyriaTel Customer Churn Analysis
<img src="images/SyriaTel.jpg">
<b>Author:<b/> Samwel Kagwi


**## Business Understanding**
SyriaTel, a telecommunications company would like to reduce money spent in the event of loosing customers and acquistion of new customers. The task at hand is to use machine learning algorithms to be able to predict the likelihoold of a customer churning from SyriaTel. Churning refers to when a subscriber cancels, stops or does not renew a subscription service.

## Data Understanding
The utilized dataset was source from Kaggle.

### Data Preparation
The following steps were taken to prepare the data:
- Checking for missing or duplicated values
- Checking the data types
- Converting columns of the object data types, to a numerical data type.
- Dropping columns that were irrelevant to this project ('area_code').

## Modelling

- Baseline model: <code>Logistic regression</code>
- Model 2: <code>Decision tree</code>
- Model 3: <code>KNN</code>
- Model 4: <code>Random forest</code>

### Evaluation Metric
I chose to use Recall as my evaluation metric.
The recall score is true positive divided by the true positive plus the false negative. It is the measure of actual observations which are predicted correctly. I chose this metric because we want to capture as many positives as possible, and doing so would reduce the number of false negatives. In this case, a false negative would be the number of customers identified as churned, but were classified as not churned. 

---

### Model 1: Baseline Model
<img src="images/baseline_model.png">

Results:
- Recall Score (did not churn): <code>75%</code>
- Recall Score (chur): <code>76%</code>

### Model 2: Decision Tree
<img src="images/decision_tree.png">

Results:
- Recall Score (did not churn): <code>98%</code>
- Recall Score (churn): <code>67%</code>

### Model 3: KNN
<img src="images/knn.png">

Results:
- Recall Score (did not churn): <code>80%</code>
- Recall Score (churn): <code>60%</code>

### Model 4: Random Forest
<img src="images/random_forest.png">

Results:
- Recall Score (did not churn): <code>99%</code>
- Recall Score (churn): <code>60%</code>


## Analysis
The steps for modeling went as follows: build a model, print classification report and confusion matrix for model, and finally determining the fit of the model. The 1st linear regression model did not perform as well as we had expected. To fix this, we used SMOTE to balance the data, by creating synthetic values to balance our existing data. The 2nd model showed higher scores that made this model adequate enough to use if chosen. This model was the DecisionTreeClassifier.It showed high results on the classification report and promising numbers on the confusion matrix. The 3rd and 4th models plotted were KNN and Random Forest, respectively. These models did not perform as well as the 2nd model.

## Recommendations

- Customers that called customer service at least 4 times have a significantly increased chance of churning. Managers should come up with new training techniques to help customer service representatives assist these disgruntled customers.

- Carry out further investigations on why customers with international plans have a higher percentage of churning.

- The firm should get more balanced data in order to improve the classification models.

- The firm should look into more variables that may have an effect on churn, such as: gender, regions and age-group.

# Repository Contents
├── images: images used in PPT and readme

├── .gitignore

├── CONTRIBUTING.md

├── LICENSE.md

├── README.md: project information and repository structure

├── Working_Notebook

├── churn_data: data used for modeling and analysis

├── notebook.pdf

├── presentation.pdf

├── presentation.ppt: Non-technical Presentation for Stakeholders

├── student.ipynb: jupyter notebook used for modeling
