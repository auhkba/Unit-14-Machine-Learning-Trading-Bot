# Unit-14-Machine-Learning-Trading-Bot

### Conclusions - Baseline Algorithm ( SVC ) - ***Senario 1***
With regards to Support Vector Machines (SVC(),default setting with  kernal = ‘rbf’) model, it has similar return patterns as “Actual Return” 

Since 2019, the trend is still similar, but its accumulated return has consistently outperformed “Actual Return’.

![base_case](Resources/svm_base_case.png)

From “Classification Report” ,  the model has high recall rate (0.96) in predicting 1.0, meaning it has high accuracy on predicting stock’s  “positive” return , however it has very poor (0.04) accuracy in predicting stock’s “negative” return (-1.0).

Overall it has around 0.50 accuracy. 

![svm_class](Resources/new_class.png)
---

### Turn the Baseline Algorithm - ( Training Dataset ) - ***Senario 2*** 

By changing the training dataset from 3 months (baseline) to 24 months, all other variables remains unchanged (only testing dataset is reduced accordingly), we see its similar patterns as Baseline Case,  but it managed quite well when the stock suffered large negative returns during 2020, 

![s1](Resources/svm_24m_train.png)

---
### Turn the Baseline Algorithm - ( SMA features ) - ***Senario 3***

By increasing both  SMA windows from `4 & 100` to `10 & 250`, we see since the beginning 2019, it outperforms “Actual Return”, which we can not see from Senario 1 & 2. However, it subsequently consistently underperforms “Actual Return”. 

![s2](Resources/svm_10_250_windows.png)

---
### LogisticRegression Model Algorithm - ***Senario 4***

With regards to a new model of Logistic Regression, it has outperformed “Actual Return” since 2019. it also starts to out-performs the Baseline Algorithm (Scenario 1), and Senario 2 & 3.  With the exception of early 2021, it starts to poorly predict stock’s ‘positive’ return.

![log](Resources/logistic_case.png)

Overall, this model improve the success rate (recall rate improved 0.04 to 0.33)  from  of predicting -1.0 (stock negative return), which maybe could explain it has better performance than other scenarios during ***flat*** market (during 20018-2020)

![new_class](Resources/new_class.png)



