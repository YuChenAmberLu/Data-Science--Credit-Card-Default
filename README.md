# Analysis of Default of Credit Card Clients Against Their Background

Analysis of credit card cardholders' background using Machine Learning on both quantitative and qualitative responses. This dataset contains information on default payments, demographic factors, credit data, history of payment, and bill statements of credit card clients in Taiwan from April 2005 to September 2005.

## Abstract
To find out the best fit algorithm for amount of given credit in NT dollars against other factors, which are important variables using Bayesian information criterion.

## Exploratory Data Analysis
To generate insights of "Default of Credit Card Clients Dataset", the first step is Exploratory Data Analysis. I performed initial investigations on the data and summarized statistics and graphical representations using `ggplot2` in R.

## Quantitative factors as responses
Machine learning on amount of given credit in NT dollars against other factors.

There are 24 factors against amount of given credit. In order to aviod overfitting, I selected the most important factors using forward stepwise selection and chose Bayesian Information Criterion (BIC) for determining the cross-validated prediction error. The Bayesian Information Criterion (BIC) gives unnecessary variable much greater penalty, so it can more efficient to aviod overfitting. 

Five algorithms and the libraries used:

<center>
  
|               Algorithms                                |        Libraries      |
|-------------------------------------------------------- | :-------------------: |
| Linear regression                                       | lm                    |
| Regularized generalized linear models                   | glmnet                |
| Classification tree                                     | tree                  |
| Bagging Approach - Bootstrap aggregating                | randomForest          |
| Boosting                                                | gbm                   |

</center>


## Qualitative factors as responses
Machine learning on whether the payment defaults next month against other factors.

And then, I did the same process on whether clients default payment next month against others factors.

Seven algorithms and the libraries used:

<center>

|               Algorithms                                |        Libraries      |
|-------------------------------------------------------- | :-------------------: |
| Generalized linear model                                | glm                   |
|Linear discriminant analysis - LDA                       | MASS                  |
| Quadratic discriminant analysis - QDA                   | MASS                  |
| K-nearest neighbors                                     | class                 |
| Generalized additive model                              | gam                   |
| Classification tree                                     | tree                  |
| Regularized generalized linear models                   | glmnet                |

</center>

## Conclusion
1. More credit card defualt for limit balance about 10000. It might mean that credit card might be too easy to be issued for people who have low credit scores. The variance of the default rate for limit balance over 500,000 NTD is higher than other range of limit balance.

2. It is lower default rate for cardholders have higher education level. Moreover, the default rate for clients whose age over 60 was higher than mid age and young people.

3. The best fit algorithm for predicting limit balance is bagging approach.

4. The best fit algorithm for predicting whether a client default next month is classification tree.


## Citation
Yeh, I. C., & Lien, C. H. (2009). The comparisons of data mining techniques for the predictive accuracy of probability of default of credit card clients. Expert Systems with Applications, 36(2), 2473-2480.

## Reference
1. https://bradzzz.gitbooks.io/ga-dsi-seattle/content/dsi/dsi_05_classification_databases/2.1-lesson/assets/datasets/DefaultCreditCardClients_yeh_2009.pdf
2. https://gerardnico.com/data_mining/stepwise_regression
3. http://www-math.mit.edu/~rmd/650/bic.pdf
