# **Product Recommender**

**DEPRECATION WARNING**

This code example was intended for use by the legacy Skafos platform and is no longer being maintained. On 05/29/2019, a new version of [Skafos](https://skafos.ai) was released, streamlining model delivery to the edge. 

[Sign-up](https://dashboard.skafos.ai/sign-up) for an account, [join](https://join.slack.com/t/metismachine-skafos/shared_invite/enQtNTAxMzEwOTk2NzA5LThjMmMyY2JkNTkwNDQ1YjgyYjFiY2MyMjRkMzYyM2E4MjUxNTJmYmQyODVhZWM2MjQwMjE5ZGM1Y2YwN2M5ODI) our Slack community, and explore some [example models](https://github.com/skafos/colab-example-models) to get started.

---


The following repo contains example code for training a product recommendation model on Skafos based on the [Recommendation Engine Quickstart](https://github.com/skafos/TuriRecommender) model. For this example, we used data from [**Thingiverse**](https://www.thingiverse.com/): a community where users interested in the world of 3D printing technology share different 3D models they have created. We built and deployed a model on Skafos to generate personalized recommendations of 3D models to users.

## What is here?
The components of this repo are:
-  `product_recommender.ipynb` - a Python notebook that trains and saves a product recommendation model. It walks through the steps of data collection, model training, and deployment.
-  `utilities/` - a directory that contains helper functions used by `product_recommender.ipynb`.
-  `requirements.txt` - a file describing all required Python dependencies.

## About the model
-  The product recommender is trained on open Thingiverse data retrieved with their [**REST API**](https://www.thingiverse.com/developers). Users can "like" different 3D model designs. This *interaction* data was used for model training. Here is a snippet of what this data looked like:

|   userId | thingId    |
|---------:|:-----------|
|        1 | 343455   |
|        1 | 345353   |
|        2 | 643363   |


-  The model can generate personalized recommendations to a user based on which 3D model designs they like and ones that others have liked.
-  In order to get data from the Thingiverse API, you must register a developer account with them.
-  Thingiverse API Python wrapper ~ adapted from: https://github.com/hroncok/thingiverse
