# end-to-end-tumor-detection
ML-Model-Flask-Deployment
This is a demo project to elaborate how Machine Learn Models are deployed on production using Flask API

Prerequisites
You must have Scikit Learn, Pandas (for Machine Leraning Model) and Flask (for API) installed.

Project Structure
This project has four major parts :

model.py - This contains code fot our Machine Learning model to predict brain tumor based on training data in which consist of images of yes and no tumor file.
app.py - This contains Flask APIs that receives employee details through GUI or API calls, computes the precited value based on our model and returns it.
request.py - This uses requests module to call APIs already defined in app.py and dispalys the returned value.
templates - This folder contains the HTML template to allow user to enter img file and displays the predicted weather the gven brain img is having a tumor or not.
Running the project
Ensure that you are in the project home directory. Create the machine learning model by running below command -
python model.py
This would create a serialized version of our model into a file model.pkl

Run app.py using below command to start Flask API
python app.py
By default, flask will run on port 5000.

Navigate to URL http://localhost:5000
You should be able to view the homepage as below : alt text

Enter valid numerical values in all 3 input boxes and hit Predict.

If everything goes well, you should be able to see the predcited salary vaule on the HTML page! alt text

You can also send direct POST requests to FLask API using Python's inbuilt request module Run the beow command to send the request with some pre-popuated values -
python request.py
