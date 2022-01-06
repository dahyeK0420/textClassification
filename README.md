# Text Classification with Text-Embedding and Classification Models

**Author Name:**  Dahye kim

**Last Edited:** 25 Apr 2021

This notebook performs a topic classification task with 3 variations in target, 2 variations in trainset size, 2 different text pre-processing configuration, and 2 different classification algorithms. The overlook of all the variations is as follow: 

* 2 Trainsets with the size of 1000 and 54,000+ observations 
* 2 Classification Models: **Logistic Regression** and **simple Recurrent Neural Network** with varying configuration based on the size of training data set
* 3 classification binary targets: Math, InfoTheory, and CompVis
* 2 Text pre-processing configurations: 
  * **WordPunktLemmatizer**: WordnetLemmatiser and WordPunctTokenizer, context independent stopwords are removed 
  * **RegexSNBTokenizer**: SnowBallTokenizer combined with RegexTokenizer with the regular expression of r"[a-zA-Z]+(?:[-'][a-zA-Z]+)?", context-independent stopwords are removed, all tokenised words with the length of less than 2 is removed, bigrams included 

In total, 24 models were trained and validated using the test data set. To evaluate the performance of all classifiers, I used a group bar plot showing accuracy, precision, recall and F-1 score 

Through creating 24 different models with variations in sample size, text pre-processing, class imbalance and classification algorithm, the program analyses the effect of each variation to the classifier performances. Based on the evaluation metrics of accuracy, recall, precision, and F-1 score, the logistic regression classifier with the target InfoTheory performed the best out of all the models. The sample size, choice of algorithm, and target class proportion impacted the performance of the models the most. However, the text pre-processing of text when using RNN might have violated the assumption on dependence of each observation (words in a document), and therefore, the model might show a different result when using different pre-processing methods. The text pre-processing configurations did not seem to have significant impact to the model performances. 
