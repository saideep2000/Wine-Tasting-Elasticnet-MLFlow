# Wine Tasting with ElasticNet in MLOps.

## Tools and Technologies:

- MLFlow


## Resources

**[Wine Tasting Mlops](https://www.youtube.com/watch?v=-NOIWzjJK-4&ab_channel=DSwithBappy)**

![Parallel Coordinates Plot](assets/image.png)
*Parallel Coordinates Plot*

## Steps Taken:


conda create -n mlops python=3.8 -y 

conda activate mlops

pip install -r requirements.txt

pip install --upgrade pippip install --upgrade pip

pip install certifi

python3 example.py

python3 example.py 0.1 0.2

python3 example.py 0.1 0.6

mlflow ui

pip install dagshub


## For Dagshub:

import dagshub
dagshub.init(repo_owner='saideep2000', repo_name='Wine-Tasting-Elasticnet-MLFlow', mlflow=True)

import mlflow
with mlflow.start_run():
  mlflow.log_param('parameter name', 'value')
  mlflow.log_metric('metric name', 1)

https://dagshub.com/saideep2000/Wine-Tasting-Elasticnet-MLFlow.mlflow


## MLflow on AWS

### MLflow on AWS Setup:

Login to AWS console.

Create IAM user with AdministratorAccess

Export the credentials in your AWS CLI by running "aws configure"

Create a s3 bucket

Create EC2 machine (Ubuntu) & add Security groups 5000 port

### Run the following command on EC2 machine :

``` bash

sudo apt update

sudo apt install python3-pip

sudo pip3 install pipenv

sudo pip3 install virtualenv

mkdir mlflow

cd mlflow

pipenv install mlflow

pipenv install awscli

pipenv install boto3

pipenv shell


### Then set aws credentials
aws configure


#Finally 
mlflow server -h 0.0.0.0 --default-artifact-root s3://mlops-buc01

#open Public IPv4 DNS to the port 5000


#set uri in your local terminal and in your code 
export MLFLOW_TRACKING_URI=http://ec2-3-88-12-55.compute-1.amazonaws.com:5000/

```