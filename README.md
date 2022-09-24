# CombinedLinearAndLogisticRegression
This repo combines both Linear and Logistic Regression algorithm into one Python module. Enjoy!

### Software, Tools, and prerequisits
1. Access to Google Colab or some Jupyter Notebook.
2. Basic python programing.
3. Basic arithmetic & calculus knowledge

### Intro: What is Linear Regression?
This deals with understanding the pattern/ slope of a given dataset given the assumption that the dataset has a linear pattern. Basically predicting the value of a variable based off the value of another variable.

Given a formulars, 
1. Equation of a line:
$$\hat{y} = wx + b$$
2. Mean Squared Error $(MSE)$, also happens to be the cost function:
$$MSE = \frac{1}{N} \Sigma_{i=1}^n({y}-\hat{y})^2$$ 
$$J(w,b) = \frac{1}{N} \Sigma_{i=1}^n({y}- (w_{i}x + b))^2$$
3. and the derivitive of the cost function, with respect to both the weight and bias respectively:  
$$\frac{dJ}{dw} = \frac{1}{N} \Sigma-2x_{i}({y}- (w_{i}x + b))$$
$$\frac{dJ}{db} = \frac{1}{N} \Sigma-2({y}- (w_{i}x + b))$$

The derivitive (negative graidient) of the cost functions tells us which direction to go to minimize the loss/ cost function which happens to be the $MSE$ in this example.

<img
  src="reg_example.png"
  alt="Alt text"
  title="Optional title"
  style="display: block; align: center; margin: 0 auto; max-width: 180px">

### Intro: What is Logistic Regression?
This is really similar to Linear Regression. Please refer to this repo for more on [Linear Regression](https://github.com/ccibeekeoc42/Basic_LinearRegression). 

This deals with creating probabilities rather than a specific value.  understanding the pattern/ slope of a given dataset given the assumption that the dataset has a linear pattern. Basically predicting the value of a variable based off the value of another variable.

Given a formulars, 
1. Equation of a line:
$$y = wx + b$$
2. The Sigmoid function:
$$s(x) = \frac{1}{1 + {e}^{-wx + b}}$$
$$\hat{y} = s(y) = \frac{1}{1 + {e}^{-x}}$$
3. The cross enthropy, also happens to be the cost function:
$$J(w,b) = J(\theta) = \frac{1}{N} \Sigma_{i=1}^n({y}^{i}log(h_{\theta}(x^{i})) + (1 - y^{i})log(1 - h_{\theta}(x^{i}))$$
3. and the derivitive of the cost function, with respect to both the weight and bias respectively:  
$$\frac{dJ}{dw} = \frac{1}{N} \Sigma 2x_{i}({y}- (w_{i}x + b))$$
$$\frac{dJ}{db} = \frac{1}{N} \Sigma 2({y}- (w_{i}x + b))$$

The derivitive (negative graidient) of the cost functions tells us which direction to go to minimize the loss/ cost.

For both the linear and logistic regression, with each itiration, we have an update rule for the new weight & bias to minimize the cost function and this update rule is given by:
$$w = w + \alpha . dw$$
$$b = w + \alpha . db$$
where $\alpha$ is the selected learning rate which tells us how fast or slow to go in the direction of gradient. This needs to be optimal as too big or too small learning rates can lead to non convergence to the global minimum error.

### Steps to completing the project
1. Import the necessary modules/ packages needed for this project.
2. Generate your dataset and split them into train & test sets.
3. Plot your dataset for visualization.
4. Implement the linear regression algorithm using np arrays ($fit(X,y)$ & $predict(X)$):
    * Initialize your weight vector to random values.
    * initialize your bias.
5. Implement the logistic regression algorithm using np arrays ($fit(X,y)$ & $predict(X)$):
    * Initialize your weight vector to random values.
    * initialize your bias.
6. Apply the sigmid to your output.
Test your regressor & evaluate the error using the $MSE$.