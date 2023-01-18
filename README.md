# Predicting Victims of Identity Theft Using Logistic Regression

## Table of Contents
* [Introduction](https://github.com/Liyaft/identity-theft-classification/edit/main/README.md#introduction)
  * [Topics Covered](https://github.com/Liyaft/identity-theft-classification/edit/main/README.md#topics-covered)
  * [Tools Used](https://github.com/Liyaft/identity-theft-classification/edit/main/README.md#tools-used)
* [The Data](https://github.com/Liyaft/identity-theft-classification/edit/main/README.md#the-data)
* [Exploring the Database](https://github.com/Liyaft/identity-theft-classification/edit/main/README.md#exploring-the-data)
  * [Questions of Interest](https://github.com/Liyaft/identity-theft-classification/edit/main/README.md#questions-of-interest)

# Introduction
The goal of this project is to predict which customers of a large bank are most likely to become victims of identity theft following a data breach. This was done by creating a logistic regression model to classify customers based on whether or not they would become identity theft victims.
## Topics Covered
  * Descriptive Statistics
  * Logistic Regression
  * Data Visualization
## Tools Used
  * JMP
  * Tableau 
# The Data
The dataset provides information on customers who were involved in a past data breach and whether or not they became victims of identity theft. It includes the following variables:
  * IDTheftVictim (response): Whether the customer becomes an identity theft victim or not.
  * DirectDeposit: Does the customer use direct deposit?
  * ATMCard: Does the customer use an ATM card?
  * DebitCard: Does the customer use a debit card?
  * PreauthorizedDebts: Does the customer use preauthorized debts?
  * AutomatedPhoneSystem: Does the customer use the bank's automated phone system?
  * ComputerBanking: Does the customer use the bank's online banking system?
  * InPersonBanking: Does the customer use the bank's in person banking?
  * ByMailBanking: Does the customer use banking by mail?
  * PhoneBanking: Does the customer use banking by phone?
  * ChgPassReg: Does the customer change their passwords regularly?
  * UseStrongPass: Does the customer use strong passwords?
  * MonitorBankStmt: Does the customer monitor their bank statements?
  * MonitorCCStmt: Does the customer monitor their credit card statements?
  * MonitorCredreport: Does the customer monitor their credit report? 

# Exploring the Data
## Questions of Interest
  * [Does the way a customer banks (online, in-person, by phone, by mail, using an app) have an impact on their risk of becoming an identity theft victim?](https://github.com/Liyaft/identity-theft-classification/edit/main/README.md#the-way-customers-bank)
  * [How do password habits (changing passwords regularly, using strong passwords) help protect customers from identity theft?](https://github.com/Liyaft/identity-theft-classification/edit/main/README.md#password-habits)
  * [Does monitoring financial statements regularly help protect customers from identity theft?](https://github.com/Liyaft/identity-theft-classification/edit/main/README.md#monitoring-financial-statements-and-reports)
  * [How accurate is the logistic regression model? Is it better at predicting victims or non-victims?](https://github.com/Liyaft/identity-theft-classification/edit/main/README.md#the-logistic-regression-model)

### The Way Customers Bank
Customers have five options when it comes to how they bank. They can either bank online, in-person, by mail, by phone, or use a mobile app. To compare the risk levels of these five different ways, I compared the response variable (IDTheftVictim) versus the five independent variables (ComputerBanking, InPersonBanking, ByMailBanking, PhoneBanking, AutomatedPhoneSystem). 

<img width="700" src="https://user-images.githubusercontent.com/117689127/213285247-867e65dc-8735-4d3d-8d4b-623c33ed4ac6.png">

Here we can see that a majority of the customers did not become victims of identity theft regardless of their banking method. However, I found that when customers use computer banking, the risk of identity theft occurring is higher at 33.3%, while customers who do not use computer banking are less likely to have their identity stole at 10.6%. The likelihood of identity theft occurring is approximately the same when they use the bank's automated phone system versus when they do not (19.6% and 19.2% respectively). The likelihood decreases when in-person, by mail, and by phone banking are used.

### Password Habits 
The dataset includes information on the password habits of customers. Using this data, we can see the likelihood of identity theft based on whether or not a customer uses strong passwords and if they change their passwords regularly. 

<img width="700" src="https://user-images.githubusercontent.com/117689127/213292078-a16f69e6-cf83-4d40-85df-da8fbfff68e2.png">

The likelihood of identity theft decreases when customers change their passwords regularly and use strong passwords versus when they do not. 

### Monitoring Financial Statements and Reports
To compare the difference monitoring financial statements makes, I compared the response variable (IDTheftVictim) versus MonitorBankStmt, MonitorCCStmt, and MonitorCredreport. 

<img width="700" src="https://user-images.githubusercontent.com/117689127/213292689-6a8acf04-5565-4000-8113-c9aeae0066df.png">

The likelihood of identity theft decreases when customers monitor their financial statements versus when they do not. 

### The Logistic Regression Model
By creating a ROC curve, I found that the area under the curve was 0.816. This means that the model is able to accurately distinguish between identity theft victims vs. non-victims approximately 82% of the time. The confusion matrix model displays a misclassification rate of 0.1676, a sensitivity of approximately 64% and a specificity of approximately 85%. Using these factors, we are able to determine that the logistic regression model is better at predicting non-victims rather than victims of identity theft.  

<img width="250" src="https://user-images.githubusercontent.com/117689127/213293404-67a44698-cee1-4c5f-a598-58970186d60c.png"> <img width="200" src="https://user-images.githubusercontent.com/117689127/213296783-f038fb6b-5734-47cf-8661-989a55d98e47.png">

