# Sentiment_Analysis
Basic sentiment analysis and binary classification (positive or negative) of an Amazon review dataset, comparing both RNN and Naive Bayes approaches 

** Comparing both approaches: 
The RNN approach had a best model accuracy of 86.5%, but had signifigantly slower speed. On the other hand, the Naive Bayes approach had a best model accuracy of 83.5%, but was extremely fast. While RNN is a bit more accurate, the Naive Bayes is the algorithm I would use in real life due to its much lower processing time, import in domains like mobile app development. RNN probably derives its improved performance from the LSTM unit used, which provides a level of memory and context to data. 

** Recurrent Neural Network & Long Short-Term Memory
In this approach, I use text vectorization with a recurrent neural network made of an embedding layer, two bidirectional long short-term memory layers, and two dense layers.

Adding more parameters and epochs naturally increased the duration. Model 8 took the longest to process. Performance seemed to vary greatly. Adding a bidirectional layer probably slightly increased accuracy, but this effect was not resilient considering the dip in performance with model 8. Model 9, with the most parameters, has the best performance. Its processing time was also shorter, but this was mostly due to external variations in computational resources more than model differences.
Log of iterations: 
SCCE = Sparse Categorical Cross Entropy 
BCC = Binary Cross Entropy
<img width="810" alt="Screenshot 2023-07-29 at 5 48 36 PM" src="https://github.com/MayaAmelieSeale/Sentiment_Analysis/assets/140470683/125f5dd6-19e0-4701-aa8d-6479f48c29ec">

Model 9 is the most succesful, and below are model 9's history plots: <img width="521" alt="Screenshot 2023-07-29 at 5 50 00 PM" src="https://github.com/MayaAmelieSeale/Sentiment_Analysis/assets/140470683/02f5e26c-2d37-4931-9800-4a3fdc01334e">

In addition, here are some examples of reviews it had trouble classifying: 
<img width="805" alt="Screenshot 2023-07-29 at 5 50 54 PM" src="https://github.com/MayaAmelieSeale/Sentiment_Analysis/assets/140470683/3d245a50-90f1-402e-b6b8-79825c278a9c">

** Naive Bayes 

Naive Bayes classifiers based on the bayes assumption of feature independence. All of the models, being that they are types of Naive Bayes, took very little computational time. It was hard to notice the computational time, much less any difference. Model performance was variable. Tfid vectorizer gave improvements over count vectorizer. Ultimately, Multinomial NB produced the best accuracy. Ultimately, this is the method I would use in real life. This is because it is much faster than the RNN approach, especially useful in mobile devices.

Log of iterations: 
G = Gaussian  |  MN = Multinomial | B = Bernoulli | C = Complement Naive Bayes
alpha = Smoothing Parameter | F = False | T = True 
<img width="808" alt="Screenshot 2023-07-29 at 5 53 15 PM" src="https://github.com/MayaAmelieSeale/Sentiment_Analysis/assets/140470683/44ddbeb3-6295-467a-a001-14a90a383ca0">

Model 11 proved to be the best, and it's confusion matrix and ROC curve are below: 

<img width="511" alt="Screenshot 2023-07-29 at 5 54 00 PM" src="https://github.com/MayaAmelieSeale/Sentiment_Analysis/assets/140470683/d35422d2-5e41-49dc-ac02-5ceaa2b96d0a">



