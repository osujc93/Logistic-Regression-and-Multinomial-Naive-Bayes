<h2 align="center">Spam Email Detection Using Logistic Regression and Multinomial Naive Bayes</h2>
<p align="center">Logistic Regression is a model that is commonly used for binary classification tasks. It models the probabilities of the default class of binary response variables through the logistic function, expressed as:</p> 

<h4 align="center">$$P(Y = 1 | X )=1\frac{1}{1 + e^{-z}}$$</h4>

<p align="center">$z$  is a linear combination of the features  $X$ , defined by:</p>
<h4 align="center">$$z=β_{0}+β_{1}X_{1}+β_{2}X_{2}+⋯+β_{n}X_{n}$$</h4>

<p align="center">$β_{0}$ , $β_{1}$ ,…, $β_{n}$  are the parameters of the model, and  $X_{1}$, $X_{2}$,…, $X_{n}$  are the features.
We fit the model to the training data  $X_{train_features}$ and labels  $Y_{train}$ , and to make predictions on both training and testing sets. The accuracy of the model on the training set is calculated and stored in  $acc_{train}$, and the accuracy on the test set is stored in  $acc_{test}$.</p>

<p align="center">A confusion matrix is generated to visually assess the performance of the classifier. This way we can show how many predictions were correct and how many were misclassifications.</p>





<p align="center">Multinomial Naive Bayes is a variant of Naive Bayes designed specifically for text documents, assuming that the features (words) have multinomially distributed data. It is great for classification tasks involving discrete features such as word counts or frequencies.</p>

<p align="center">The probability of a document being in class  $c$:</p>
<h4 align="center">$$P(c | d) \propto P(c) \prod_{i=1}^{n} P(t_i | c)^{x_i}$$</h4>

<p align="center">$P(c|d)$ is the posterior probability of class $c$ given document $d$.</p>
<p align="center">$P(c)$ is the prior probability of class  $c$.</p>
<p align="center">$P(ti|c)$ is the conditional probability of term $i$ occurring in class $c$.</p>
<p align="center">${x_i}$ is the frequency of term $i$ in document $d$.</p>
<p align="center">The Multinomial Naive Bayes classifier is applied to TF-IDF transformed text data. The classifier is trained on the feature matrix  $X_{train_features}$  and the labels  $Y_{train}$ , and it predicts the labels of both the training and testing datasets. Similar to Logistic Regression, the accuracies of the predictions are calculated for the training and testing sets and recorded in  $acc_{train}$  and  $acc_{test}$ , respectively.</p>

<p align="center">A classification report is generated providing a detailed breakdown of precision, recall, f1-score for each class, and a confusion matrix is displayed to visualize the performance of the classifier, highlighting the correct and incorrect predictions across different classes.</p>
