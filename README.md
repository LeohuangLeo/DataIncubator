Data source is from kaggle: https://www.kaggle.com/mohansacharya/graduate-admissions
I use Python 3.7 to do analysis. Here is the way I analyzed this data:
1. Read file.csv file and check if the data has null value and extreme value.
2. Use correlation function to know that the usefulness of the feature data. From plotting image, I can see that 'Serial No.'    is a useless feature.
3. Split the datasets into training and validation data. (each sub-data has their corresponding feature data and target data)
4. Use Sciki-learn to train the data.
5. Data normalization can increase training speed and accuracy of the data.
6. Use linear regression as  model to train the data. (In this datasets, it's enough to use linear regression because the data    is continuous and the number of features are not large)  
7. Here are two parameters I can adjust to find the optimal model : polynomial degree and regularization function. (linear        regression in Sciki-learn have default setting in number of epochs, so I would not change epoch)
8. 
  (1). Accuracy performance when it comes to different polynomial degree:
  Increasing polynomial degree will let model to track every single data as much as possible. This is easy to get high    accuracy in training and validation data. However, keep increasing polynomial degree will cause overfitting. Thus, the model   cannot correctly predict the data that the model haven't seen before.
  
  (2). Accuracy performance when it comes to different scale of regularization function(alpha):
  Regularization (R2) can smooth the model so that we can decrease the influence of extreme value. However, too large scale of R2 is not good because it will cause underfitting. From the plotting result, I got best accuracy in validation when alpha = 100.
