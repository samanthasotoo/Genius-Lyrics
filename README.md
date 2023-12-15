# Genius Lyrics Pipeline
# CIS 4130
Samantha Soto 
![image](https://github.com/samanthasotoo/Genius-Lyrics/assets/42002045/8d494af9-9164-4a92-b30a-533578eb2d10)

## Description

In this project, I explored the Genius Lyrics dataset, which houses information on a song, including the lyrics, the genre, the artists, the features, and the language. After carefully exploring the data, I focused on creating a pipeline that predicts the genre of a song based on various attributes such as lyrics, artist information, language, and other features of that nature. In creating my pipeline, I created features such as sentiment analysis to enhance my predictor further. 


The initial step involved transferring the data to Amazon S3 using an EC2 instance, the AWS CLI, and the Kaggle API.
After data exploration, I transitioned to Databricks Community Edition for feature engineering due to AWS billing constraints. This involved preliminary cleaning of the song lyrics and converting the data from a pandas data frame to a Spark data frame, followed by saving it in Parquet format for more efficient processing.
Feature engineering consisted of removing structural words like 'chorus' and 'verse', indexing categorical features, and applying OneHotEncoding. I then tokenized the lyrics and conducted sentiment analysis to create numerical features. These steps culminated in the application of a multinomial logistic regression model, initially trained to predict genres within the rap category.
The next phase was to scale the model to predict across a broader range of genres by processing a larger dataset on an EMR cluster. However, this step was met with JVM OutOfMemoryErrors due to limitations in Java heap space. Financial and time constraints, alongside the complexity of configuring the recommended Sandbox environment, led to the decision to pause the project's scaling efforts despite the belief that the model’s accuracy would improve with larger data.

My notebooks are split up into cleaning & uploading to cloud storage and feature engineering & visualization. 

Tools Used:
- AWS EC2
- AWS S3
- Community Databricks
- Python
- PySpark
  
