########################################################################################################################################################
9 JUNE 2022

README FOR R CLASS 3 WEEK 4 PROJECT
########################################################################################################################################################

The script run_analysis.R takes the following eight datasets and merges six of them into one master original (raw) dataset.
The last two datasets are used to define variable names and activity labels.

1) subject_train.txt	This dataset contains 7352 subject numbers between 1 and 30 for the train data (some digits are contained in subject_test.txt).
2) y_train.txt		This dataset contains 7352 activity numbers between 1 and 6 for the train data.
3) X_train.txt		This dataset contains 7352 subjects and 561 variable measurements for the train data.
4) subject_test.txt	This dataset contains 2947 subject numbers between 1 and 30 for the test data (some digits are contained in subject_train.txt).
5) y_test.txt		This dataset contains 2947 activity numbers between 1 and 6 for the test data.
6) X_test.txt		This dataset contains 2947 subjects and 561 variable measurements for the test data.
7) features.txt		This dataset contains 561 variable measurement names used for both train and test data.
8) activity_labels.txt	This dataset contains activity names corresponding to numbers 1 to 6.


The datasets are merged, rearranged, and tidied in five major steps, the first of which is described below. The others are in CodeBook.md.

--------------------------------------------------------------------------------------------------------------------------------------------------------
PART 1
--------------------------------------------------------------------------------------------------------------------------------------------------------
The first six datasets are merged together, making one master original dataset with 10299 rows and 563 columns.

The Train dataset (7532 x 563) is created according to the following steps:
1) Column 1 is from subject_train.txt.
2) Column 2 is from y_train.txt.
3) Columns 3 - 563 are from X_train.txt.

The Test dataset (2947 x 563) is created according to the following steps:
1) Column 1 is from subject_test.txt.
2) Column 2 is from y_test.txt.
3) Columns 3 - 563 are from X_test.txt.

The Original dataset (10299 x 563) is created by stacking Train on top of Test.
Next, Original is ordered in ascending order by Column 1 and then Column 2 (so subjects ordered 1 - 30 and for each subject, activity ordered 1 - 6).
Note that the column headers are currently V1 for subject, V1.1 for activity, v1.2 for the first variable (originally called V1), and V2-V561 for
all remaining variables. These names will be changed in a later step.


--------------------------------------------------------------------------------------------------------------------------------------------------------
Parts 2 - 5 are in CodeBook.md.
--------------------------------------------------------------------------------------------------------------------------------------------------------
