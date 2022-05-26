## Telco churn project
• Telco co churn ratio is at 27% while the industry average is at 21%

#### Goals for this project:

• Determine what are the key drivers leading to customer churn

• Build a Machine learning model that is able to predict customers with a propensity to churn

• Draw takeaways from the data

• Issue recommendations


![exec_summary.png](https://raw.githubusercontent.com/lincolnmuriithi11/Project_Classification/c76b2fab4f4ae24fd218c9fcd0e75912af16ba37/exec_summary.png)

## Project approach
• Create an acquire.py file that makes the project duplication process feasible

• Data acquisition, preparation, exploratory data analysis and statistical testing, modeling, and model evaluation

• Report Key findings and recommendations

• Construct a model to predict customer churn using classification
techniques.

• Give a 5-minute presentation to stakeholders

## Project deliverables
• Jupyter notebook report

• Acquire.py file

• Readme file explaining the project

## Data dictionary
![telco_df.png](https://raw.githubusercontent.com/lincolnmuriithi11/Project_Classification/main/data_info.png)

## Data preparation
• transformed the total_charges column from a string to an integer for workability purposes.

• discovered nulls in the total_charges column where I opted to drop them since they are less than

• columns to be encoded into boolean values. "Yes" = 1, "No/No internet service" = 0. (online_security, online_backup, device_protection, tech_support, streaming_tv, streaming_movies)
1% of the dataset

• cleaned up some of the columns that had spaces and replaced them with an underscore

• dropped all the columns that contained id. ('payment_type_id',
'internet_service_type_id','contract_type_id','customer_id','phone_service’).

• on the train dataset I chose to up sample the data because churn_Yes variables were underrepresented at 26% while the churn_No was at 74%. Ths meant that the data was learning more from the non-chrners than the churners.

• lastly, used get dummies on on boolean columns to ensure ML model capability

• split the data to Train, validate and test

• all the necessary functions are available on the acquire.py file

## Train Data
![train.png](https://raw.githubusercontent.com/lincolnmuriithi11/Project_Classification/main/train_info.png)

## Hypothesis

• Hypothesis 1

• alpha = .05

• $H_0$: Method of payment does not have any effect on whether a customer will churn or not

• $H_a$: customers with electronic check type of payment are likely to churn more than any other method of payment

• Outcome: I rejected the Null Hypothesis; there is a high positive between the method of payment and the churn rate.

## Hypothesis

• Hypothesis 2

• alpha = .05

• $H_0$: tenure does not have any effect on whether a customer will churn or not

• $H_a$: customers with tenure below one year(new customers) are likely to churn more than customers past the year mark

• Outcome: I rejected the Null Hypothesis; customers under the one- year tenure mark are one of the highest rated churn groups .

## Summary

• I ran 3 machine learning models : Knearest Neighbors, Decision Trees, and Random Forests

• I decided to go with random forests because it had the highest accuracy on both the train and validate predictions

## Conclusion & Recommendations

- #### due to a high churn rate for customers on month to month contracts incentivize them to switch to yearly contracts
- #### introduce semi annual contracts

- #### discontinue/discourage electronic check payment system for payment purposes (risky: highest number of customers)

- #### have package deals for services to  promote online security, online backup to internet customers

- #### possibly introduce surveys to measure customer satisfaction with the services like tech support




## What can we do with more time?
- #### since fiber optic customers have a high churn rate, we can possible collect industry data and see why the customer have a propensity to churn and what the competition is offering 

- #### lastly, matching the competitions prices on month to month customer prices might heavily reduce the churn rate
