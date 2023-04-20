# **Credit Card Market Segmentation**

---

* ### Ingrid Arbieto Nelson

# **Overview :**<a name='Overview'>

---
![image](iStock-1137281183.jpg)

[**Image credit**](https://www.istockphoto.com/portfolio/alexialex?mediaty)
## **Chosen Dataset : Predicting Credit Card Customer Segmentation** 

### **Part 1**

---



#### **1 Source of data**
*  [Credit Card Customer Segmentation](https://www.kaggle.com/datasets/thedevastator/predicting-credit-card-customer-attrition-with-m)
   * [The Devastator](https://www.kaggle.com/thedevastator)

#### **2 Brief description of data**

*This dataset contains a wealth of customer information collected from within a consumer credit card portfolio, with the aim of helping analysts predict customer attrition. It includes comprehensive demographic details such as age, gender, marital status and income category, as well as insight into each customer’s relationship with the credit card provider such as the card type, number of months on book and inactive periods. Additionally it holds key data about customers’ spending behavior drawing closer to their churn decision such as total revolving balance, credit limit, average open to buy rate and analyzable metrics like total amount of change from quarter 4 to quarter 1, average utilization ratio and Naive Bayes classifier attrition flag (Card category is combined with contacts count in 12months period alongside dependent count plus education level & months inactive). Faced with this set of useful predicted data points across multiple variables, capture up-to-date information that can determine long term account stability or an impending departure; therefore, offering us an equipped understanding when seeking to manage a portfolio or serve individual customers.*

#### **3 What is the target?**

*The target is whether the bank customer will churn.*

**Attrition_Flag:** *Flag indicating whether a customer has churned out*

#### **4 What does one row represent? *(A person? A business? An event? A product?)***

*Each row represents a bank customer.*

#### **5 Is this a classification or regression problem?**

*This is a classification problem. The goal is to determine whether the bank customer has churned or not. This is a yes or no question.*

#### **6 How many features does the data have?**

*There are 20 features.*
<br />

#### ***Features:***

---  

![image](https://drive.google.com/uc?id=1BdR6oZbzLq5_G7bSbuDTgzO9MsNfHnWH)
![image](https://drive.google.com/uc?id=1K9EBqKt0tl-nPodKxe822cirt7l7dhW-)
<br />

# **Explanatary Data Analysis**
## **Average Utilization Ratio vs Total Revolving Balance**

---
![image](https://drive.google.com/uc?id=1HPnBfkPdWPI4ypEp8P9fwRtRkHRbe33G)

* ### As Average Utilization Ratio for credit card customers increases toward the maximum Total Revolving Balance, there is more attrition.
* ### There is a strong positive correlation between Average Utilization Ratio and Total Revolving Balance.

## **Income Category vs Total Revolving Balance**

---
![image](https://drive.google.com/uc?id=1FlezR3ZSWtjOgZq78qxX3TKoGC_5lysg)

* ### Credit card customers with $0 balance tend to exit the credit card company.
* ### Credit card customers with a range of total revolving balance leave credit card, with slight bubble at maximum Total Revolving Balance.

## **Average Amount Available to Buy vs Average Utilization Ratio**

---
![image](https://drive.google.com/uc?id=1XOhYT0ZKfGNgriU9oiHEfdl-TiQZBFyE)
### **Average Open to Buy** : The difference between the credit limit assigned to a cardholder account and the present balance on the account.
* ### Credit card Customers using less credit available have more credit available to purchase, yet choose to exit the credit card company.
* ### Incentiving those with higher average dollars available to buy could decrease attrition from the credit card company.

## **Final Model Selection**

---

#### The best model is the SMOTE Random Classifier model, *without PCA*.
   * #### By optimizing for class imbalance, this improves the Test Recall from 74% to 79%. Recall tells you the False Negatives. In this case, a False Negative is where the model predicts the credit card customer would not leave but the credit card customer actually does leave! We want to minimize False Negatives.
   * #### Precision score is slightly less, down from 90% down to 84%, but a False Positive is not such a bad thing. This would mean the Model predicted that the customer would leave but customer stayed with the credit card company.
   
* #### The SMOTE default Random Forest Classifier has an accuracy of 94%, the same as the prior optimal model. 


![image](https://drive.google.com/uc?id=1vSoweC715HpQEgZW1jDDvFAEaAN1ryvZ)

![image](https://drive.google.com/uc?id=1SivhfQhPqoiuu-SjKAygIKOBX70jsDNP)

## **Final Recommendations for Credit Card Attrition**

---


1. #### Marketing to those with lower Average Utilization ratio, higher Card class could prevent customers from leaving credit card company.
2. #### Credit card customers that do not carry a balance are more likely to leave credit card company. These customers may have been inactive or have contacted us recently. Sometimes contacting us indicates dissatisfaction. Offering incentives could entice these customers to utilize more credit, resulting in more profit for credit card company.
3. #### Those with more Available balance to Buy (better credit, higher incomes) often leave credit card company. Marketing to these income classes could help in retaining more customers.
