Getting and Cleaning Data Course Project CodeBook

This file describes the variables, the data, and any transformations or work that you performed to clean up the data.

The source data is download from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip. 

A full description of the source data is available at http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones.

run_analysis.R does the following:
- Read 'X_test.txt', 'y_test.txt' and 'subject_test.txt' and combine them to 'test_set' variable.
- Read 'X_train.txt', 'y_train.txt' and 'subject_train.txt' and combine them to 'train_set' variable.
- Combine 'test_set' and 'train_set' into  'complete_set' variable.
- Extracts only the measurements with text'mean' or 'std' into 'complete_set_of_mean_and_std' variable.
- Uses descriptive activity names to name the activities in the data set by replacing numeric activity_label to descriptive activity name:
1 -> WALKING
2 -> WALKING_UPSTAIRS
3 -> WALKING_DOWNSTAIRS
4 -> SITTING
5 -> STANDING
6 -> LAYING
- Labels the data set with descriptive variable names by replacing all "." with "_". 
(To peer reviewers, I don't think adding seperater like "_" and replacing "acc" with "accelerometer" adds any values. 
Such conversions only make the readers hard to match / search from original source data's definition files.)
- An independent tidy data set with the average of each variable for each activity and each subject is set to 
'average_of_mean_and_std_for_each_activity_and_each_subject' variable.
