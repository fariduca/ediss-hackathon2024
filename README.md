# EDISS Hackathon 2024

The task of the hackathon was to come up with a problem statement with the data at hand and provide a solution to the problem. The data of the hackathon was comprised of two datasets, a real-world scenario and a simulation scenario. The simulation data comes from the [SimuSafe Project](https://www.mdu.se/en/malardalen-university/research/research-projects/simusafe-simulator-of-behavioural-aspects-for-safer-transport). Both datasets had the same structure and set of features. The features included the position data on the track, scenario parameters, the drivers’ neurophysiological variables, and the car parameters like speed, yaw, acceleration, etc.

## Our approach

One of the questions we wanted to explore was can a classification model learn to predict the violation type based on other features in the dataset. To test this, we used 7 columns that indicate emotion as target variables and everything else as labels. Because we were not interested in the driver, we dropped the ‘subject’ and ‘start time’ columns. Also, we dropped the rows with incomplete data that contain nulls and scaled the dataset using standard scaler. We chose the Multi Output Classifier and Random Forrest Classifier to
train on our data. In order to evaluate the performance of the model we used the sklearn.metrics methods accuracy_score and humming_loss.
