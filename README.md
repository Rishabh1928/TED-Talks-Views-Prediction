# TED-Talks-Views-Prediction

TED Talks: TED is devoted to spreading powerful ideas on just about any topic. These datasets contain over 4,000 TED talks including transcripts in many languages. Founded in 1984 by Richard Salman as a nonprofit organization that aimed at bringing experts from the fields of Technology, Entertainment, and Design together, TED Conferences have gone on to become the Mecca of ideas from virtually all walks of life. As of 2015, TED and its sister TEDx chapters have published more than 2000 talks for free consumption by the masses and its speaker list boasts of the likes of Al Gore, Jimmy Wales, Shahrukh Khan, and Bill Gates.

## Problem Statement

The main objective is to build a predictive model, which could help in predicting the views of the videos uploaded on the TEDx website.

## Data Overview

●	Number of instances: 4,005

●	Number of attributes: 19

Features:

●	talk_id: Talk identification number provided by TED

●	title: Title of the talk

●	speaker_1: First speaker in TED's speaker list

●	all_speakers: Speakers in the talk

●	occupations: Occupations of the speakers

●	about_speakers: Blurb about each speaker

●	recorded_date: Date the talk was recorded

●	published_date: Date the talk was published to TED.com

●	event: Event or medium in which the talk was given

●	native_lang: Language the talk was given in

●	available_lang: All available languages (lang_code) for a talk

●	comments: Count of comments

●	duration: Duration in seconds

●	topics: Related tags or topics for the talk

●	related_talks: Related talks (key='talk_id',value='title')

●	url: URL of the talk

●	description: Description of the talk

●	transcript: Full transcript of the talk

●	Views: The number of views for each talk 

## Steps involved

●	Exploratory Data Analysis

●	Null values Treatment : Our dataset contains around 400 null values which might tend to disturb our mean absolute score hence we have performed KNN nan value imputer for numerical features and replaced categorical features nan values with the value ‘Other’. We chose to impute nan values and not drop them due to the size of the data set.

●	Encoding of categorical columns: We used Target Encoding for replacing the values of categorical variables with the mean of the views. This was done to not increase the dimensions to the data set while also keeping the relationship of variables with views into consideration.

●	Feature Selection: For Feature Selection we have done the following: we have introduced new numerical features from the categorical features,combined features and also we have used f_regression in which we have taken the features with the maximum f-scores.

●	Outlier Treatment: We have done outlier treatment on variables like duration and occupation. This was done by replacing outliers with the extreme values at the first and third quartiles. We have done outlier treatment to prevent high errors that were influenced by outliers.

●	Modelling & Hyperparameter Tuning











