## 1. What is the problem?
The mortality number in the fifth wave of covid 19 in Hong Kong will be explored in this project with Python.

## 2. What is the data and where does it come from?
In this project, the datasets are the fifth-wave situation of reported cases of COVID-19 in Hong Kong and collected from DATA.GOV.HK website which are coordinated by the office of the Government Chief Information Officer.

## 3. How do you solve the problem?
The collected datasets are split into 4 different CSV files after consolidation and analysis. 
Firstly, we loaded the 5th wave statistics single day with age dataset into dataframe "df". Secondly, the COVID-19 number final dataset was loaded into dataframe "df2". Thirdly, the vaccination date total final dataset was loaded into dataframe "df3". Lastly, the received and unvaccinated dataset was loaded  into dataframe "df4". 

After loading the datasets into dataframe, we merge “df”, “df2”, “df3” into “combinAll” dataframe to observe the real data situation. Moreover, we plotted the bar chart and line chart of the mortality number in the fifth wave from 10th March to 31th March.

On the other hand, “df2”, “df3” and “df4” dataframes are combined into “combind234” for building up a model. We split the "combind234" dataframe 0.7 as the training set and 0.3 as the test set. We set features and labels both in the training set and test set. Finally, we built Multiple Linear Regression, gradient descent function and k-NN algorithm to solve the problem.

## 4. Why do you choose the selected algorithm(s) to solve the problem?

Firstly, we use the features (Date, Confirm, Asymptomatic Infection, RAT, Total, Dose_daily_total, Received of the Death and Unvaccinated) to predict the label (total of death). In addition, the features and labels are numerical data, therefore we choose the multiple linear regression algorithm. The target of multiple linear regression is to model the relationship between the explanatory variables and response variables. 

In addition, we have the learning rate (alpha) in the multiple linear regression model. Therefore, we use gradient descent to update the parameters of our model because it is an optimization algorithm which is commonly-used to train machine learning models. We had set up 4 different functions including “predicted_label”, “loss function”, “dldw” and “dldb“ function for preparing build up gradient descent function and prediction. 

Finally, we use the k-NN algorithm to solve the regression problem. We set the number of neighbors and k-value both to 15 to fit the k-NN model. Besides, we use two line charts to explain the accuracy and error rate of the k-NN algorithm. 

## 5. How good is the result?
Multiple linear regression has the highest accuracy in the three algorithms. 
The value of mean square error (MSE) which close to zero will represent better quality of the regression model, the MSE of the multiple linear regression is 1.730986214884963e-27. On the other hand, R squared represents the model's strong intensity, the R squared of the multiple linear regression is 100. This result can explain that the model has the highest persuasiveness and most optimization prediction between three algorithms. The table below shows that the prediction results of the test set are exactly the same with the real data.

![image](https://github.com/Leong15/MachineLearning_Project/assets/53085228/fb0a13b2-980e-4624-a2b4-f909ffac1608)




## 6. Conclusion
### A. Gradient descent 
![image](https://github.com/Leong15/MachineLearning_Project/assets/53085228/5bb58f2e-42ac-4f8f-83e7-7ebd4521985e)
![image](https://github.com/Leong15/MachineLearning_Project/assets/53085228/1af78b3a-5d9e-4832-b005-3e37e21d6abf)


### B. kNN algorithm

![image](https://github.com/Leong15/MachineLearning_Project/assets/53085228/e1873d42-3c05-4f11-97ab-613451fd8b5b)
![image](https://github.com/Leong15/MachineLearning_Project/assets/53085228/c1e7ae7c-b3d2-4814-8f5e-09a428d33237)


After all the processing, we can see the performance of the three algorithms. The Multiple Linear Regression has the best performance in this data. The Gradient descent has the second-best performance. The comparison of the actual label and predict label can find out the accuracy is pretty well and we can see the graph of loss vs epoch, the loss almost 0 when the iterations are around 125. So, even the gradient descent is not the best solution but still a pretty decent algorithm for this data.

k-NN algorithm is the worst algorithm in this project. When the number of neighbours is increasing, the accuracy of the training dataset is decreasing. The accuracy of the testing dataset keeps unchanged and the value is equal to 0 all the time.

## Reference

“Archive of Statistics on 5th Wave of COVID-19” (2022, March 31), The Government of the Hong Kong Special Administrative Region, Retrieved April 1 ,2022 from https://www.coronavirus.gov.hk/chi/5th-wave-statistics.html#

“Data in Coronavirus Disease (COVID-19)”(2022, March 31), DATA.GOV.HK, Retrived April 1, 2022 from https://data.gov.hk/en-data/dataset/hk-dh-chpsebcddr-novel-infectious-agent

