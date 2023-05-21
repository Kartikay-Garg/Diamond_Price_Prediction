# End to End Machine Learning Project
![ineuron-logo](https://github.com/Kartikay-Garg/Diamond_Price_Prediction/assets/117899107/d8eed903-4774-4b7a-b577-c60be632e43e)

## Diamond Price Prediction

> About the Data : The goal is to predict price of given diamond (Regression Analysis).

> There are 10 independent variables :

>> id : unique identifier of each diamond 

>> carat : Carat (ct.) refers to the unique unit of weight measurement used exclusively to weigh gemstones and diamonds. 

>> cut : Quality of Diamond Cut 

>> color : Color of Diamond 

>> clarity : Diamond clarity is a measure of the purity and rarity of the stone, graded by the visibility of these characteristics under 10-power magnification. 

>> depth : The depth of diamond is its height (in millimeters) measured from the culet (bottom tip) to the table (flat, top surface) table : A diamond's table is the facet which can be seen when the stone is viewed face up. 

>> x : Diamond X dimension 

>> y : Diamond Y dimension 

>> z : Diamond Z dimension 

> Target variable:

>>price: Price of the given Diamond.


### Created an environment

```
conda create -p venv python==3.8 -y
```
### Activated the environment
```
conda activate venv/
```
### install all necessary libraries in requirements.txt
```
pip install -r requirements.txt
```

## For Deployment: (AWS Elastic Beanstalk) (step by step) make: make a folder: .ebextension>python.config>
~~~
option_settings:
  "aws:elasticbeanstalk:container:python":
    WSGIPath: application:application
~~~   

Then, make a folder then application.py> copy full code of app.py and then push it on Github. 
~~~
1. open aws then sign in
2. Search for Elastic Beanstalk open application icon
3. create application
4. application name: , platform = python
5. click on sample application then create application
6. search on aws, "codepipeline", click on CodePipeline, create pipeline, pipeline name: , click next
7. source provider: Github (version 1), click connect to the Github, confirm it
8. select repository name, branch: main, Github webhooks, click next
9. Build Provider: Skip
10. Deploy provider: AWS Elastic Beanstalk, region, application name, environment name, next
11. Review: create pipeline
12. if error occurs: delete app.py file
~~~
### Deployment Success.


## For Deployment: (Azure)
~~~
1. open azure, sign-in, create the resource
2. create Web App, subscription name:, resource group:, name:, publish: code, runtiome: python 3.8, next
3. continuous deployment: enable, configure with your github account, organisation: github username, repository: repo name, branch: main, review+create, create
4. wait then reload github project page.
5. .github/workflows will be created on your repository, click on it
6. .yaml fill would be created
7. go to github actions, add or update azure....
~~~
### Deployment Completed.
