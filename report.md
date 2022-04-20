## 2.1 - LinearRegression().fit(): 

- Given a set of data points, this function finds the best fit line for the data. 
- It tries to minimise the cost function, which is the sum of the squared errors between the predicted and actual values. 
- This function takes x and y coordinates as input and retures a best fit linear model wrt to the type of data that was present in x. In general, the model will output the coefficients of an n<sup>th</sup> degree polynomial, where n is the number of columns of X (passed as a parameter). If x is a list of pairs ( for ex [[1,1],[2,4],[3,9]...) then it will result in a quadratic equation model of form ax<sup>2</sup> + bx + c.  

- Various parameters may be passed to this function. Some of them are:
1. X (2D array/matrix): x-coordinates of the data points
2. Y: y-coordinates of the data points 
3. fit_intercept: It indicates whether or not we have to calculate the intercept. If this is set to true, then the intercept will be calculated. Otherwise, the line is assumed to pass through origin.
4. copy_X: The X matrix will be copied if this is set to true (default). 
5. n_jobs: no of processors to be used for computation. By default, only one is used. 
6. positive: If this is set to true, then the regression coefficients are forced to be positive. 

It returns the following: 
1. coef_: the estimated coefficients of the regression line. 
2. intercept_: the estimated intercept of the regression line. 

## 2.2.2 - Explanation for the change in bias and variance: 
- As the function varies from lower degree to higher degree, the bias decreases and becomes almost constant as the degree is further increased. This is because, initially the polynomial is under-fit and the bias is high. However, if we increase the degree beyond the best-fit degree, then overfitting occurs and the model will fit the data points better than necessary, thereby reducing the bias beyond what is optimal. 

- The variance of the model increases as the degree increases. Initially, it is low as the model is of low complexity(underfit), therefore, the  variance is low. As the degree increases, complexity of the model increases, therefore the variance increases (above the optimal value as we cross the best-fit polynomial).  

## 2.3 - Why irreducible error does not change on varying degree of class function?

- Irreducible error is the amount of noise in the data, therefore it does not depend on our choice of the model. In this case,irreducible error was only caused by the calculation errors that are caused. So it does not depend on the degree of class function. As the computer is very accurate in calcuating irreducible error is a small quantity ( in the range of 10<sup>-10</sup>). 

## 2.4 Graph Observations: 
 - The following are observed from the graph: 
1. From the graph, we can see that a third degree polynomial is the best-fit for this data. 
2. For degrees one and two, the model is underfit. Therefore, the bias is high and the variance is low. 
3. For the degree 3, the total error is minimum from which we can infer that the 3 degree polynomial model is the best fit.
4. As the degree is increased, beyond 3, the model is now overfit. Therefore, the variance increases and the bias decreases. 
5. As the degree is further increased, the bias becomes constant but the squared bias increases slightly. 
6. The data is continuous and cost of house varies as a function of the cube of the area of house.  
