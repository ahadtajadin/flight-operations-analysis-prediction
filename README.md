# Flight Operations Analysis & Prediction

## About the project:

For this project, I used flight data from January 2025 to look at flight delays and see whether I could use machine learning to predict them.

I used Python to clean the data, look for patterns and create some charts. I then built two machine learning models and compared how well they performed.

## Dataset:

The dataset contains 539,747 flight records from January 2025.

Some of the information in the dataset includes:

- Airline
- Departure and destination airports
- Scheduled departure time
- Departure and arrival delays
- Whether the flight was cancelled
- Flight distance

The original CSV file is not included because it is too large to upload to GitHub.

## What I looked at

I started by checking the dataset for missing values and cancelled flights then removed cancelled flights and created a new *Delayed* column. I counted a flight as delayed if it left more than 15 minutes later than scheduled.

Next, I looked at how delays varied between:

- Airlines
- Airports
- Scheduled departure times

One thing I noticed was that flights later in the day generally had higher delay rates than flights in the early morning.

## Machine learning

I built two classification models using the Scikit-learn module:

- Logistic Regression
- Decision Tree

For the prediction part, I used information that would be available before a flight departed:

- Airline
- Origin airport
- Destination airport
- Scheduled departure hour
- Flight distance

I didn't use actual departure or arrival delays as features because those would only be known after the flight had started.

## Results

The test accuracy for each model was:

| Model               | Accuracy |

| Logistic Regression | 59.04% |
| Decision Tree       | 82.24% |

At first, the Decision Tree looked much better because it had a higher accuracy.

However, when I looked at the classification report and confusion matrix, I found that it was barely identifying flights that were actually delayed.

Logistic Regression had a lower accuracy, but it detected around 60% of the flights that were actually delayed.

This showed me that accuracy isn't always enough when the data is imbalanced. Looking at things like precision, recall and F1-score gave me a better idea of how the models were performing.

## What I learned

The main thing I learned from this project was how to take a large dataset and work through the whole process myself, from cleaning the data to building and evaluating a machine learning model.

I also learned about:

- Data cleaning
- Data analysis with Pandas
- Data visualisation with Matplotlib
- Categorical variables
- Classification
- Logistic Regression
- Decision Trees
- Model evaluation
- Confusion matrices
- Precision, recall and F1-score

## Tools I used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook
- VS Code
- Git
- GitHub

Overall, this personal project has helped enhance my programming knowledge and develop new skills.
