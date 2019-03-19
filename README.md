# Disaster Response Pipeline Project

This project is a way to help responders during a crisis sift through messages they receive, and categorize what the message is saying quickly. This is to reduce the already heavy burden on responding agencies in a disaster and so that they can address and parse all the information coming at them. The training dataset was provided by FigureEight.

A message only needs to be inputted into the web app and it will be assigned to the relevant categories. 

### Instructions to run web app:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`


### Built with:

Bootstrap - web framework used

Flask 

### Notes

This particular pipeline isn't quite accurate. One of the challenges was the long training time when looking for optimal parameters, the parameters that were checked were just how many n_neighbors the classifier took. There is a lot more room for optimization in that space. 

