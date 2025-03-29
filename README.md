# Goal:
The goal of the project is to develop and compare four machine learning models—Logistic Regression, Decision Tree, SVC, and KNN—to predict customer response to a bank's marketing campaign (whether they will subscribe or not).

# Business Objective: 
Increase the success rate of marketing campaigns by targeting the right customers, optimizing resource allocation, and boosting conversion rates, ultimately improving ROI for the bank.

# Exploratory Data Analysis: 
The dataset contains around 411K rows and had 21 columns of which 10 were numerical and rest categorical.
None of the columns had empty or null values 
there are 5 numeric columns 
 age,duration,campaign,pdays,previous -  have to be checked for any outliers - No need for Coercing 
pdays - 999 means client was not previously contacted - This needs to be properly interpreted. Can be replaced with 0
there are 5 columns with float data type
emp.var.rate, cons.price.idx, cons.conf.idx, euribor3m,  nr.employed -  have to be checked for any outliers - No need for Corcing 
![numericalfeatures](https://github.com/user-attachments/assets/8e9e0b4b-66ca-424c-9142-d4b3ac7e472b)

 10 columns with categorical values - which can be coerced using label encoding 
 job,marital, education,default,housing, loan, contact, month, day_of_week, poutcome
 Default , Housing and loan are Binary values 
Admin, Blue_collar and technician contributed to most of job data
Marital status - Unknown seems to be not present at all
University degree holders seem to contribute more to the Campaign
Default - has many unknown values
housing- yes and no values seems to equally distributed
loans - most people who denied have no loans
contact - most people contacted through cell phone
month - May month had the most campaigning happened
Days of the week - seems to be equally distributed
poutcome- those who were not called previously seems to be contributing more and also
![categoricalfeatures](https://github.com/user-attachments/assets/e3098b35-978f-4a1d-a5a1-8b936b197868)

# Baseline model: 
This seems to be a imbanaced class . Hence we consider the baseline accuracy as 88.65%
![Baseline](https://github.com/user-attachments/assets/7bfffcc0-4f07-4235-92f4-b88af142033e)

# Simple model and Score: 
A simple logisticregression model is fit and the accuracy came to 90% which is better than baseline accuracy 

# Model comparisons: 
![Compare](https://github.com/user-attachments/assets/0cd472f8-c477-42c1-84d8-228f706be804)


From the above comaprison, the SVM model seems to be the best overall model. It has the best test accuracy, precision, recall, and F1-score, but the training time is a drawback.
If fast training time is a requirement then KNN can be used. It is very fast with a slightly lower performance than SVM but still gives good accuracy and F1-score.

# Improving the Model :

Feature Engineering :  #pdays does not seem to be contributing much to the prediction and hence can be dropped and model can be trained again 
Hyper Parameter tuning and Grid Search : Tried doing the same for all 4 models , however its taking long time and hence could not get to completion. But have placed the code in jupyter notebook. 
Performance metric: Since grid search is taking huge time , couldnt get to the performance metric after tuning. 
