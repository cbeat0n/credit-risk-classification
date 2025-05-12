# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Classifying for the type of loan customer is incredibly important in the financial industry. For personal, business, home, or auto loans, loans are widely used and it is necessary to make sure the person in question is a healthy or high risk applicant. The last thing wanted is a bank or financial offerer to give out an option for someone to either default or fail to pay the loan back. Thus, the classification problem begins here.

* Credit health is aggregated along many factors including but not limited to the size of the loanb(loan_size),the interest rate at hand (interest_rate), the borrower's income	(borrower_income), depending on the field itself their debt to income ratio	(debt_to_income), the number of accounts that they hold	(num_of_accounts),	if they have bad marks on their accounts (derogatory_marks), and any other total debt they may or may not have	(total_debt). Financial health is important and also very hard to lay down depending on the amount of information used so these columns are representative of a majority of someone's health but do not technically include everything. There may be other factors that other situations might require that are not used here. All of these factors are then accounted for to calculate whether someone is Healthy or High Risk.

* The total amount of data is about 77 thousand rows. The mean loan amount was about 9800 dollars with 7.3% interest rate. Unfortunately the average debt to income was 0.377 and income 49.2k. Most people had 3-4 accounts with 0-1 derogatory marks and 19.2k in debt. Despite this, a majority of people did succeed in being healthy applicants.

* Simply put we first pulled the csv with Path() and then created a dataframe to represent this data.Then, we used  train-test-split to split the training testing data along 0.25 and allowed us to train and then test the data appropriately. Lastly, we then trained and predicted on the model with surprisingly great results.

* Due to the sensitive and also not black and white nature of classification of consumer credit data, I used a Logistic Regression model. This allowed to classify the data while not inherently separating it, regressing it along probability values and then splitting it along the 0.5 line. This is a good model because it is understandable and accurate at the same time (high explainability and usability).

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Logistic Regression:
    * Below you will see that the precision and recall for Healthy (0) loans are near pefcet, with the support being the majority of the dataset. Below this you find that (partially due to support size) the precision and recall on Risky loans (1) is slightly lower, at 0.84 and 0.94. This is weaker but still reasonably strong. Overall, the accuracies are over 0.9 each, going from 0.92 to 0.97 and 0.99 twice.
    *  precision    recall  f1-score   support

     Healthy       1.00      0.99      1.00     18765
       Risky       0.84      0.94      0.89       619

    accuracy                           0.99     19384
   macro avg       0.92      0.97      0.94     19384
weighted avg       0.99      0.99      0.99     19384

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Although we only used Logistic Regression, this would likely perform the best due to the nuance it allows for, mentioned earlier. Compared to other classification methods, it is more flexible and this allows it to be of a higher accuracy.
* Performance does not depend on the type of problem we are solving, ie financial vs medicine. In this case I will say that the precision and recall on 1's would likely be higher if the support was higher, however.

I would recommend testing other classification models to either confirm or deny the usage of Logistic Regression or other models if it is not costly to the business in question.
