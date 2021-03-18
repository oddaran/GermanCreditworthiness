# GermanCreditworthiness
Analysis of German Credit dataset (available at ftp.ics.uci.edu/pub/machine-learning-databases/statlog)
In this project, we describe some data from observations of 1000 applicants for credit worthiness in Germany. 30 variables are given, with ratings of “good credit” or “bad credit.” The predictor variables will be evaluated for their ability to predict good or bad credit risk. We analyze which of the variables are the best predictors of “good credit.”

We look at exploratory functions.  Proceed with five examples to describe the data. Extract number of predicted good/bad cases.  We check to see if n/a values exist in predicted cases. We check variable type for outcome variable 'RESPONSE,' which are all integer values.  Now we can process data further by partitioning for training/validation sets.
After partitioning the data, we run the logistic regression functions of the trained data.

Next we evaluate the classification of our logistic regression model, where RESPONSE is the predictor. We create lift and gain charts (see germancreditworthiness.docx), along with decile-wise chart.  This answers the question: how far into the validation data do you go to get maximum net profit? (otherwise specified as a percentile rounded to deciles.)

Then, create a confusion matrix to find true positives and true negatives of the model.  Determined the accuracy of this matrix at 0.7325.

Then, we run another classification model using CART (classification and regression trees).  We first plot the classification trees of training and validation data. Upon this, we generate another confusion matrix of the models, until we reach accuracies of 0.8233 and 0.695, respectively.

Summary
To improve our performance by changing the cutoff. We can use the "predicted probability of success" in logistic regression as a basis for selecting the best credit risks first, followed by poorer risk applicants. First sort the validation data on "predicted probability of success." For each validation case, calculate the actual cost/gain of extending credit. Should this logistic regression model be scored to future applicants, the "probability of success" cutoff of 0.5 can be used in extending credit.
