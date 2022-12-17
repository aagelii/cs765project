# cs765 final project

First install the necessary packages by running:

pip install -r requirements.txt

After that, make sure you have the ATUS data downloaded in the same directory, i.e. atussum_0321.csv and codes.xlsx

Now, you can simply run the cells in project.ipynb.

There are pretrained models saved in /models/, to use them simply ignore cells with "model.fit()" in them.

To load a specific model, use model.load_model("/models/model-" + (activity) + (number) + ".txt")

Or you can retrain models from scratch by runnning all the code

--------------------------------------------------------------------------------------------------------

There are 17 models in this project, each is a regression gradient boosted decision tree for each activity. It outputs the 
predicted fraction that activity takes in a day, so to get the minute count you must multiply the value by 1440 (total minutes in a day).

For the activity name translation see translate.txt for translations of abbreviations, the activities are the major categories from https://www.bls.gov/tus/lexicons/lexiconwex2020.pdf 

The image MAE.png shows the Mean Absolute Error for each model

In the directory pred_distribution contains the graphs created showing the distributions of the actual data vs the predicted distribution

In the directories male_dist and female_dist, you'll find graphs comparing the distribution of the male/female data run throught the predictors vs the original data

