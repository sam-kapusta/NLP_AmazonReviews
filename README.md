# NLP - Amazon Reviews Star Rating Predicter 

**Goal**: Predict the aggregate product rating on an Amazon product

There are a couple of steps needed before making a classifier to predict the aggregate rating. The 1st is to create a language model that understands the specific English that is being spoken in reviews (which is different from everyday conversation, Wikipedia, text conversations, etc.). 

I also wanted to see the difference between predicting individual comments ratings and the combined rating on an Amazon product, 
as there is a lot of individual varience with why people rate comments a certain way (ex. User speaks highly of a product and gives it 3 stars) that is removed with the Wisdom of the Crowd. I really like how Wikipedia describes this phenomenon "there is idiosyncratic noise associated with each individual judgment, and taking the average over a large number of responses will go some way toward canceling the effect of this noise."

### 4 Sections:

Created a Language Model that understands Amazon product reviews by using Transfer Learning on the WikiText 103 dataset, model can predict corect next word in sentence 1/3 times.

Created a Classification Model that predicts star rating given on individual Amazon product reviews with a 55.7% accuracy. 

We can't actually measure our final classification model with accuracy as the average star product on a rating is not one of [1,2,3,4,5] but rather a number somewhere in that range. Thus, we retrain our model with the metric of mean_absolute_error and getr an mean_absolute_error of .6.

Succesfully trained classification model in predicting aggregate star rating on an Amazon product to a mean error rating of .3.
For example, if a product is rated at 3.9, on average the model will predict 3.6 or 4.2

### Notes
- Ran on Fast.ai Deep Learning library which is built on top of Pytorch and contains sub-libraries for vision, nlp, tabular, and collab
