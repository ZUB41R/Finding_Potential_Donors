# Finding_Potential_Donors

This is the second project submitted as part of completing the [Machine Learning Engineer Nanodegree](https://www.udacity.com/course/machine-learning-engineer-nanodegree--nd009t) by [Udacity](https://www.udacity.com/). 

The objective of this project is to implement a number of different `Ensemble Methods` and find the best one to recognize potetnial donors who can be invited to donate for a charity.

The dataset is from [UCL Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Census+Income) and has a number of input features that contain biographic, social and economic information of more than 45000 individuals. The target variable is the annual income which is expressed as above or below 50000 USD, which corresponds to a binary classification problem.

After a couple of data preparation steps such as trasnforming the skewed features into normal ones and normalising numerical features, I use one-hot encoding to make the categorical features ready for the algorithms. Later I split the data into 80:20 ratio for training and testing set respectively.

Before applying different enseble algorithms, I evaluate the model in terms of Naive predictor which provides the performance in case all of the predicted values are more than 50K. I have outlined three algorithms namely [Random Forrest](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html), [Gradient Boosting](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.GradientBoostingClassifier.html) and [K-Nearest Neighbors](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html) with their advantages and disadvantages in classification problems. Using the training and predicting pipeline prepared with these three algorithms, all of the three different sample sizes show Gradient Boosting has the best efficiency.

Furhter I use grid search to tune the hyper-parameters of `Gradient Boosting` and obtain an accuracy of 0.87 and F-score of 0.75 in the optimized model. Finally I also find out teh five most significant features that contibute in prediction.
