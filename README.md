# GCP_Dataproc_wordCounter
Counting words from a book using GCP Dataproc service

## Overview
The goal of this project is to create a fully managed Hadoop ecosystem using Google Cloud Dataproc service and perform a Pyspark job in order to count the occurences of all the words in a book.

In order to do so, the book file will be uploaded to a Cloud Storage bucket and then processed by an Dataproc cluster that will be created for this purpose. After the processing, the results will be stored in the output folder of the Cloud Storage bucket. The image below ilustrates the process:
<p align="center"><img src="./overview.png" width="500"></p>

The cluster will perform a Pyspark job that will be submitted using the ```counter.py``` file.

## Steps
* Create the Cloud Storage bucket
* Create the folder ```data/```
* Upload the book file to the data folder
* Upload the ```counter.py``` file to the bucket
* Create the Dataproc Cluster either manually or using the command from the ```dataproc_cluster_config``` file in the Cloud Shell
* Submit the Pyspark Job to the cluster by using the "submit job" button within the Dataproc Cluster
* Select the ```gs://{bucket}/counter.py``` file to run the job
* Results will be stored in a output folder in the Cloud Storage bucket
