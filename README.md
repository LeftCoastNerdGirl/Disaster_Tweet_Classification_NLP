# Classification of Twitter Disaster Tweets

From the Kaggle website:

"Twitter has become an important communication channel in times of emergency. The ubiquitousness of smartphones enables people to announce an emergency they’re observing in real-time. Because of this, more agencies are interested in programatically monitoring Twitter (i.e. disaster relief organizations and news agencies).  

But, it’s not always clear whether a person’s words are actually announcing a disaster. Take this example:  

![Screenshot 2024-08-25 at 2 18 54 PM](https://github.com/user-attachments/assets/07d50d8e-0043-4780-9412-7042139e797d)

The author explicitly uses the word “ABLAZE” but means it metaphorically. This is clear to a human right away, especially with the visual aid. But it’s less clear to a machine. In this competition, you’re challenged to build a machine learning model that predicts which Tweets are about real disasters and which one’s aren’t."   

https://www.kaggle.com/competitions/nlp-getting-started/overview  

First step was to download the data files provided and explore them. I used Pandas to load them into dataframes and then view the headings and the data.  
Next I cleaned up the data  
  The keyword and location columns did not add value to our analysis and had many empty fields so I removed them.  
  I used kpgtalkie to clean the data removing characters and information that does not add value to the training such as urls and email addresses, etc  

I made a quick pie chart to confirm that the ratio of real disaster tweets vs metaphorical use of disaster words would give us a good model. I also checked the basic features using the same tool.  

Next I explored which classification model results in the highest accuracy. I downloaded the necessary modules from sklearn, set up the test data, and ran the models showing the confusion matrix for each.  

Results, best to lesser models:  
Logistic Regression: 82.01%  
SVM: 81.81%  
Kernal SVM: 81.09%  
Random Forest: 78.53%  
Decision Tree: 73.15%  
KNN: 65.59%  

Conclusion of the model exploration - Logistic Regression provided the best results however SVM and Random Forest models were successful as well.  

I then trained a model using linear regression and exported the results.  
