# Module 12 Report 

## Overview of the Analysis

The credit_risk_classification file is trained on a chunk of the data, while some of the remaining data is saved for testing. Assuming the model works, this machine learning algorithm could be used to pridict the category of load (Healthy or High-Risk). The reference data that was fed into the machine learning algorithm was the loan size, interest rate, income, debt-to-income ration, number of accounts, derogatory marks and total debt. In order for further data to be evaluated, it would require these columns at a minimum. In future, if more borrow information becomes available, that could also be fed in and used to train the algorithm.


The algorithm that was created was trying to predict the loans that should be rated as Healthy or High Risk (meaning higher rate of defaulting). The algorithm is based on a trained regression model that is able to take in all the values, and create a weighting value of importance each piece of information (loan size, interest rate, income, debt-to-income ration, number of accounts, derogatory marks and total debt) is in determine the health rating of that loan. Initially a basic regression model (LogisticRegression) is used to see how accurate this would be, and it showed a 95% accuracy rating, however, after running the data through the RandomOverSampler, the algorithm was able to get a much more accurate idea of the importance each piece of information, and make a better call of whether that loan was risky or not.



## Results

* Machine Learning Model 1:
  * The Model 1 was very accurate at 99% accuracy, but it certaily wasn't perfect when it came to identifying all High risk loans.

  * The "Healthy Loan" class precision is 1.00, meaning it predicted "Healthy Loan" loans correctly. 
  * The recall is 0.99, which means that the model correctly identified 99% of the "Healthy Loan" loans.

  * The "High-Risk" class precision is 0.85, which means that 85% of the predicted "High-Risk" loans were truely "High-Risk" loans.
  * The recall is 0.91, which means that the model correctly identified 91% of the "High-Risk" loans.


* Machine Learning Model 2:
  * The Model 2 was also very accurate at 99% accuracy, but did a lot better with identiying High risk loans.

  * The "Healthy Loan" class precision is 1.00, meaning it predicted "Healthy Loan" loans correctly. 
  * The recall is 0.99, which means that the model correctly identified 99% of the "Healthy Loan" loans.

  * The "High-Risk" class precision is 0.84, which means that 84% of the predicted "High-Risk" loans were truely "High-Risk" loans.
  * The recall is 0.99, which means that the model correctly identified 99% of the "High-Risk" loans.



## Summary

Summarise the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
The twos models produce very similar outputs with high accuracy and low failure rates. The model 2 of machine learning using RandomOverSampler produces a higher recall rate for high risk loans. Therefore, objectively model 2 is a better model of machine learning. Due to both models having fantastic levels of recognising healthy loans, but model 2 having better detection of high risk loans, I think it makes sense to go with model 2. It is best that we can detect both high risk and healthy loans quicly and accurately.

I think it would still be a good idea to have high risk loans investigated by a human after it has been identified to ensure that the customer is able to both meet repayments, and don't have any of the negative impacts of being a high risk borrower (eg, higher interest rates, lowered credit score, etc). Where possible, we should try to downgrade any high risk to healthy if possible, while also ensuring these high risk loans will be paid.