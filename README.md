# Adobe_final

## Overview

This repository contains the final submission for the Adobe Challenge. The challenge involves behavior simulation and content generation, divided into two tasks. This README file provides an overview of the project, instructions for setup, and details about the implementation.

## Task 1: Behavior Simulation

### Description

This task focuses on behavior simulation, where the goal is to give the user, an estimated number of likes that a particular tweet will recieve on twitter if the tweet is posted on the platfrom from the community. 
Therefore, the outline of this task was to make a Machine Learning model that will simulate the people present on twitter and give a numerical value that will correspond to the number of likes it may recieve on the platform. 

### Steps to Run

Inference:
First create the BERTweet embeddings for all attributes of the content of each dataset.
This includes username , date , content , content+date+username.

the content+date+username is called combined embeddings

Feed the individual embeddings into the classifier for prediction of classes
convert these predicted classes into a csv file

load these prediction classes into the regressor script , load the regressor models,and also load the combined embeddings and predict the likes for each entry.

Training:
load the dataset into the embeddings generator. Generate the embeddings in the same manner as done in the inference section. Once the embeddings are generated, feed them into the classifier, and train the classifier. The classifier takes the individual attributes embeddings as input. Now save the weights and predict the classes. Train the individual regressors with combined embeddings as input.

## Task 2: Content Generation

### Description

This task involves content generation, aiming to generate the content of the tweet, given the metadata of the tweet, i.e. given the number of likes, content attached, time, usernames etc. predict what would be the tweet. This is beneficial if a user is not able to think about the tweet content, then it can just give the model the data and the target likes it wants, and the mdel will generate the content of the tweet.

## Way to Use


### Task 2

In this task, you have to download the three notebooks, provided in the Task 2 folder in the Notebooks folder, and the steps are as follows:

- Using the media captions generator notebook to generate the captions of the media present in the dataset. (For, the test data, captions are provided in the dataset folder under the names cc_captions for content generation for unseen company and ct_captions for content generation for unseen time period, as captions for the first task was not necessary)
- Combine the generated captions with the give data, to make a final file. (For the given data, cstc and cstt are the two file for conetnt generation for unseen company and time respectively)
- Fine tune the LlaMA-2 model using the LLaMA finetuning notebook to finetune the LlaMA model for our task.
- Using the final inference notebook, get the final generated tweets for this task. 

## Report

A detailed description for these tasks is provided in [this] () report.  