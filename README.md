# TikTok Claims Classification

# Overview
This project objective is to develop a predictive model that can determine whether a video contains a claim or offers an opinion. This project utilized a synthetic data created in partnership with the TikTok. The Random Forest model emerged as a champion model with an F1 score of ~1 and recall of 99% which performed near to perfection in classifying claims and opinions. Based on the model video view count which is related to user engagement is most influential in classifying a claim.

# Business Understanding
TikTok users can report videos that they believe violate the platform's terms of service. Because there are millions of TikTok videos created and viewed every day, this means that many videos get reported - too many to be individually reviewed by a human moderator. Analysis indicates that when authors do violate the terms of service, they're much more likely to be presenting a claim than an opinion. Therefore, it is useful to be able to determine which videos make claims and which videos are opinions. Videos that are labeled opinions will be less likely to go on to be reviewed by a human moderator. Videos that are labeled as claims will be further sorted by a downstream process to determine whether they should get prioritized for review. For example, perhaps videos that are classified as claims would then be ranked by how many times they were reported, then the top x% would be reviewed by a human each day. 

# Data Understanding
The dataset consists of `20K records and 12 features. The features included information on user engagement of a video - like count, view count, share count, donwload count, comment count, and account status of the author.

# Modelling and Evaluation
Both random forest and Xgboost models performed equally but there is a slight improved performance by the random forest. The best hyperparameter combination of the random forest predicted video_view_couunt feature as the most important feature. The model performed with a F1 score of ~1 and 99% recall. The model is not overfit as it produced similar results on the both validation and test datasets. 

# Conclusion
The model classified claims based on the user engagement of the video. As the model performed to near perfection, there is no need for further data preprocessing and feature engineering. But, it would be of high predictive factor if the dataset included user report behavior i.e. number of reports per video per user. 
