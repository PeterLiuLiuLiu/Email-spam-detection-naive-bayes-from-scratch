# Email-spam-detection-naive-bayes-from-scratch)

This project serveres as a demostration of building machine learning classifier (naive bayes) from scratch. 

The idea of Naive Bayes is to use prior probability (maybe 1/2 for this case), and modify the probability of a sentence being spam or ham through considering every word's spaminess, thus fine tuning the probability along the way as we evaluate the final posterior probability. More on this here: https://en.wikipedia.org/wiki/Naive_Bayes_classifier

Procedures of building:
1. Use the "stop words" from nltk.corpus to get rid of common words
2. Import labelled text with spam/ham from database
3. Perform data processing and data cleaninga and below is the sample data
<img width="625" alt="Capture" src="https://user-images.githubusercontent.com/96327756/172740508-726d1a5d-8127-45d6-b493-987b2bf5e4e4.PNG">
4.Divide the data into train/text 
5. Train data using bag-of-words approach with the following steps:
  a. We start from prior probabilities
<img width="277" alt="Capture" src="https://user-images.githubusercontent.com/96327756/172741384-e20b9ec7-0333-49df-a8ce-3d63029779b1.PNG">
  b. From ham, we throw the sentence into a bag and then count them, arriving at P(word | ham)
<img width="278" alt="Capture" src="https://user-images.githubusercontent.com/96327756/172741468-b6532727-35bb-4b63-802f-e665dda81ff1.PNG">
  c. From spam, same operation
<img width="284" alt="Capture" src="https://user-images.githubusercontent.com/96327756/172741579-0e6bcd61-f012-4198-8d03-a9f7a839ceb0.PNG">
6. Test data from the bag-of-word conditional probability trainned data, evalute the probability of ham and spam
  <img width="271" alt="Capture" src="https://user-images.githubusercontent.com/96327756/172741673-5773b848-69ef-4450-a877-6ad93fcd57b3.PNG">
<img width="278" alt="Capture" src="https://user-images.githubusercontent.com/96327756/172741766-514fb80e-702d-4cab-94ba-8df3bf6fac6e.PNG">
   The sentence is ham since the probability of spam is higher then ham
7. Continue doing in through all test cases and achieve an accuracy of over 98% consistently. False positive is low at around 1~2%, which is the most cared matrix
<img width="414" alt="Capture" src="https://user-images.githubusercontent.com/96327756/172742159-c3ccabc6-02f4-4c9e-82cf-2c4d2c210ea5.PNG">

