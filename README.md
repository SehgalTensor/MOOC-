# MOOC-
MOOC Data
Task Involved: Classifying whether a student will pass or fail in MOOC course depending on type of action(play, seek, load, stop or pause) taken for each video by each user.

Data Description: Train & Test files are provided. Data is given for 63 videos by 5050 users.

Feature Engineering Involves:

63 features corresponding to each video are designed. First, the count for each type of action (play, seek, load, stop or pause) is calculated for each video by each user. Then, weights are assigned for each action taken for 63 videos by 5050 users. Base weight for each action is taken as 10. If a user has played, seek, stop or paused a specific video, then its weight is assigned as 
if x=='load_video':
return 0*10
if x=='play_video':
return 0.5*10
if x=='seek_video':
return 0.23*10
if x=='pause_video':
return 0.19*10
if x=='stop_video':
return 0.07*10
if x=='speed_change_video':
return 0*10

Using this, I have calculated weight for each action taken by each user for each video and multiply it with occurrence of each action for 63 videos by each user. These weighted value for each video by each user is considered as feature set for data analysis.

I applied various classification models as 
	'Logistic Regression', 
	'Gradient Boosting', 
	'Support Vector Machine',
	'KNeighbors',
	'Decision Tree',
	'Ada Boost',
	'Bagging',
	'Random Forest'
Out of all these models, random forest has performed best according to training and testing accuracy level. Accuracy on test data is approx. 93% which is in fact great compared to other approaches where deep learning model were used earlier for same exercise.
