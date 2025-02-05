
[![CircleCI](https://dl.circleci.com/status-badge/img/gh/abderrahimsoumer/DevOps_Microservices/tree/master.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/abderrahimsoumer/DevOps_Microservices/tree/master)

## Project Overview
This project is a part of the Udacity Cloud Devops ND.

In this project, you will apply the skills you have acquired in this course to operationalize a Machine Learning Microservice API. 

You are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

## Files Explanation
- **app.py**	Python flask Apllication that return the prediction result
- **Makefile** include instructions/commands that you use to setup environment: install, tests and lint ...
- **Dockerfile** Contains the commands used to create a docker image
- **run_docker.sh** Run and build a docker image
- **upload_docker.sh** Upload docker image to docker hub
- **run_kubernetes.sh** Setup and run app on kubernetes
- **make_prediction.sh** making api call that return prediction

---

## Setup the Environment

* Create a virtualenv with Python 3.7 and activate it. Refer to this link for help on specifying the Python version in the virtualenv. 
```bash
python3 -m pip install --user virtualenv
# You should have Python 3.7 available in your host. 
# Check the Python path using `which python3`
# Use a command similar to this one:
python3 -m virtualenv --python=<path-to-Python3.7> .devops
source .devops/bin/activate
```
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl
* Start a local cluster: minikube start
* Run this command to deploy the application in kubernetes: ./run_kubernetes.sh
* Check the pod status if it is up and running: kubectl get pod
* When the pod status is runing, run this command again: ./run_kubernetes.sh
* Make predictions using: ./make_prediction.sh

Delete the cluster after your done: minikube delete
