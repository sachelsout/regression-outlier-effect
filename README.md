# regression-outlier-effect
This repository shows how outliers affect best fit linear regression line and how we can overcome this outlier problem with regularization.
<h1>What is Linear Regression</h1>

![image](https://user-images.githubusercontent.com/86348193/225282012-458c7d5c-a405-4b05-b552-ca51b226c0d1.png) <br>
Linear Regression is a machine learning algorithm based on supervised learning. It is used to predict the value of a variable based on the value of another variable. The variable you want to predict is called the dependent variable. The variable you are using to predict the other variable's value is called the independent variable. A best fit line is drawn and the errors can be calculated for it. Here, squared error/squared loss is calculated for all the datapoints. It is nothing but the squared error between the actual datapoint and predicted datapoint.<br>
<h1>What is an outlier</h1>

![image](https://user-images.githubusercontent.com/86348193/225283132-961a5fb6-aa85-4570-8095-99c16a60919e.png)<br>
An outlier is an individual point of data that is distant from other points in the dataset. It is an anomaly in the dataset that may be caused by a range of errors in capturing, processing or manipulating data. There can be multiple outliers in the dataset. Also an outlier can be informative sometimes. So we shouldn't remove the outliers before analyzing them. <br>
<h1>Effect of outliers on linear regression best fit line</h1>

![image](https://user-images.githubusercontent.com/86348193/225283896-9c2400fa-f95e-4f3e-b801-681a61dac410.png)<br>
In the above given diagram, we can see that after increasing the number of outliers, the best fit regression line tends to bend towards the outlier datapoints. So this is the adverse effect of the outliers in the dataset.<br>
<h1>Overcoming the outliers effect</h1>
To overcome the effect of outliers on the best fit regression line, there can be many methods. One of the method is to use regularization during training the data. Different regularizer (here alpha) values can be used and then the algorithm can be trained on these different regularizer values. Below are the results after using regularization.<br>

![image](https://user-images.githubusercontent.com/86348193/225285089-b1deb0a3-8a87-47c6-8920-62f92469d333.png) <br><br>
<h3><ins>Observation :-</h3></ins><br>
<ins>When alpha = 0.0001</ins><br>
As alpha value is very small, the regression line tends to outliers as number of outliers increases. For 1 or 2 outliers, the line is far away from them. But as the number of outliers increase, the line shifts towards them, considering them non-outlier points.<br><br>
<ins>When alpha = 1</ins><br>
Even after increasing alpha from 0.0001 to 1, exact same observation is seen for the line which is seen for alpha = 0.0001.<br><br>
<ins>When alpha = 100</ins><br>
As the alpha is set to 100, the regression line becomes more robust to outliers(line remains far away from outliers). As the outliers increase, it still affects the line but comparably less (compared to less values of alpha).
