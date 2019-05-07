# Project Description
For our machine learning final project, we decided to predict
[Myers Briggs personality types(MBTI)](https://en.wikipedia.org/wiki/Myers–Briggs_Type_Indicator)
using a dataset we found on Kaggle. The dataset consists of posts users made on a personality forum:
https://www.kaggle.com/datasnaek/mbti-type

<img width="1158" alt="Screen Shot 2019-05-07 at 1 30 59 AM" src="https://user-images.githubusercontent.com/40588854/57285332-db9db900-7067-11e9-8696-fa9f017efd63.png">


## Methods
First, we cleaned up the text data and created NLP features, then fit different models such as Multinomial Naive Bayes, 
Logistic Regression, Random Forest, XGBoost, LightGBM and LSTM. 

Metrics such as AUC, F1 score and accuracy were used to evaluate the performance of models. We then fine tuned our models and leveraged voting classifier to ensemble them. Finally, to build up our test set, we scraped tweets from celebrities like Obama and Lady Gaga, using our model to predict their MBTI types. The predictions look interesting.

<img width="1275" alt="Screen Shot 2019-05-07 at 1 35 43 AM" src="https://user-images.githubusercontent.com/40588854/57285633-7a2a1a00-7068-11e9-9a0c-6af3c6e582b8.png">

## Results
The data was heavily imbalanced, with most people identifying as introverted (I) and Intuitive (N)
rather than extroverted (E) and Sensitive (S). Because of this, all the models we tried 
(Logarithmic Regression, Random Forest, Multinomial Naive Bayes, SVM, LightGBM, and XGBoost) had 
trouble classifying extroversion vs introversion and intuition vs sensitivity. However, when we 
made a Voting Classifier using Logarithmic Regression, Random Forest, LightGBM, and XGBoost, we 
were able to achieve the best AUC-ROC score and f-scores.

<img width="836" alt="Screen Shot 2019-05-07 at 1 42 12 AM" src="https://user-images.githubusercontent.com/40588854/57286086-69c66f00-7069-11e9-9f96-34700c467e20.png">


## Team (alphabetical order)
Ben Khuong  
Donya Fozoonmayeh  
Nan Lin  
Tomohiko Ishihara  
Zack Pan 
