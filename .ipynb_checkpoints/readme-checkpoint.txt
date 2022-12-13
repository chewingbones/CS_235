The Gaussian Naive Bayes Classifier is designed to predict the probability that a given tuple belongs to a given class for continuous data with labels.

My Naive Bayes Classifier, naivebayes(), has three methods:

1) naivebayes.fit(X,y, mle = True, priors = [], t = None) 

naivebayes.fit() trains the model on data provided by the user.

inputs: 

a) X is a numpy array or pandas DataFrame of data to train the classifier.
b) y is a numpy array or pandas DataFrame of the labels of the data that will train the classifier.

parameters: 

a) mle (bool) is the maximum likelihood estimation. It maximizes the mean and variance for each class in the labels. By default it is set to true.

b) priors (list of floats) are the class prior probabilities. If left empty the classifier will automatically calculate the class priors from the given data.

c) t (float) is the threshold for allowing a function to be classified in the negative class for binary classification. By default the value is left empty.

2) naivebayes.gauss_predict(vectors)

naivebayes.gauss_predict() predicts the class for each tuple. 

inputs:

a) Numpy arrays or Pandas series.

3) naivebayes.predict_proba(vectors)

naivebayes.predict_proba() returns the probabilites for each tuple for each class. The probabilities are normalized to sum to 1. 

inputs:

a) Numpy arrays or Pandas series.


There are also a few attributes:

var_mean (dictionary) is the variance and mean of each attribute (or feature) in a class 
prob_c (dictionary) is the class prior probability for each class in the labels
attribute_probabilities (list) is the conditional probability of a tuple belonging to either class.
t (float) is the threshold for a tuple belonging to the negative class. It is empty by default.