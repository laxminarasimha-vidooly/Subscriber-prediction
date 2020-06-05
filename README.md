# Subscriber-prediction

Subscribers prediction-version 3-documentation

Project Name:   Subscribers prediction

Scope: Build a model for predicting subscribers count of a YouTube channel where subscribers are hidden

Business Problem:
To understand growth of a youtube channel
to perform competitor analysis
to provide industry wise growth of youtube 

Usability:
In order to achieve the above business problem, a channel will be passed through the model and value of subscribers will be predicted. Model will be said to have achieved acceptance criteria if it has less error value.

Strategy:
model needs to be built for predicting subscribers count by using public stats of youtube channel available such as channel views, uploads, last 30 days stats and other derived information 

Solution:
model’s output will be the predicted value of subscribers which can be used to populate the hidden channel subscribers. 
Versions:
version 1: testing failed due to lower accuracy level.
version 2: testing failed due to lower accuracy level.
version 3: needs to be implemented (On hold)

Data Quantity Required:
1 lakh channels data containing public stats mentioned above collected for analysis

Sources:
various youtube apis (channel stats, channel search, playlist apis)
List Of Algorithms used:
random forest regressor
random forest classifier
xgboost regressor

API Endpoints:
predicted value of subscribers along with channel id (version 1)
predicted value of subscribers along with channel id, class of subscribers range (version 2)

Expected: predicted value of subscribers along with channel id (version 3)

QA Strategy:
Testing needs to be done on known unused channels of youtube and the model is accepted if model gives at least 80% of accuracy on test data

Delivery Mechanism: (Data processing\Batch\Lambda):
model will be delivered in the form of api

Phase of Development: (Completion state\iteration):
version 3
Unable to establish statistical relationships between variables and model is not able to catch the variance of the features. Tried considering various public features of channels and last 30 days videos of channels. Segmented data into multiple parts and tried to develop different models in each segment. but, the models are not efficient in predicting the values at which the actual subscriber rate is less than 5000, between 50k and 100k and above 0.1M. 
Also, remaining model performances were between 50-60% (for 20% deviation from actual) which are below acceptance criteria. 
Updates on Version3- Used statistical analysis to further segment data and remove unwanted data pointers to reduce variance. Collecting data pertaining to channels such as comments for sentiment analysis and videos’ statistics from channels.
