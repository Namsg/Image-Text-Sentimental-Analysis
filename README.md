# Image-Text-Sentimental-Analysis
-Introduction

Sentiment Analysis is one of the rigorous field where extensive study is happening. In this digital world and specifically in social media platforms like Facebook, twitter, LinkedIn etc. people convey their thoughts or give their reactions through posts or comments.
These posts contain sometimes only images, sometimes only texts and sometimes both. And from perspective of sentiment analysis, most of the work has been done using one form of data, like only texts or only using images but not both.
Using only one type of data and make a model upon it is known as unimodal. And when we include two types of data like images and texts and make a model then it is known as bi-modal or multi-modal.

-Image Dataset

For this project the dataset is taken from publicly available dataset repository, kaggle. The description of the dataset is described below:
The dataset is combined in two categories, positive and negative. Positive contains happy and surprise categories and Negative contains anger, fear, sadness, contempt and disgust.
The dataset contains total 908 images, from which model is trained on 888 images and tested on 20 images. Further positive category has 457 images on training set and 431 images on negative category.
Next created a function which reads an image from both directory and stores it pixel values in an array.
I got 710 images for training and 178 images for validation. The shape of each input image is 48 by 48 with three channels I.e(48*48*3).

-Text Dataset

For text sentiment analysis we have used twitter dataset extracted from kaggle. The data is in the csv file format and the data consists of around 10,48,576 rows and 6 rows consisting of different features from which we need to find out the features that influence the target column and tells us about the sentiments of twitter post by performing the Exploratory Data Analysis(EDA).
The dataset contains around 1M tweets with six columns:-
 target: target column tells if a tweet is positive or negative.
 id: id is the twitter id.
 date: date tells when the tweet was posted.
 Flag: some kind of flag value while collecting the data.
 User: user tells who posted it.
 Text: text are the tweets.

- Integration model

We have a twitter dataset from which we built our text sentiment modal and we have image dataset from which we built image sentiment model. To get the overall prediction on image and text both we first create a test dataset. Because we have image data separately and text data separately and in order to test our model we need a dataset which has image and text both simultaneously.
Total test images data are 167, where 84 images are positive and 83 are negative.Since, there are 84 positive images, we extracted 84 text from this dataset where target is 1 and stored in another dataframe and added one more column of serial no I.e. 0 to 83.
The same we do to get average probability score. Then using if else, we give the overall prediction. So, if negative average probability is greater than positive probability then our prediction is negative means 0,or Else,our prediction is positive i.e 1 and appended all the prediction to a list.
The countvectorizer used for transformation is trained on the same training dataset which was used in building text model.

-Conclusion

The Image-text sentiment analysis system is one of the essential systems today and it has very important as for an image dataset it is useful for reading/analyzing the reaction(happy, sad or neutral) and text data is for analyzing reviews about any new product in market or any kind of new application reviews.
Sentiment analysis of image-text is to understand people’s position, attitude, and opinion toward a certain product
