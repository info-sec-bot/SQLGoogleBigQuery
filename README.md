<p align="left">
    <img src="img/SQL.png" alt="GoogleBigQuery"  width="300" height="200">
</p>

# SQLGoogleBigQuery
- [Overview](#overview)
- [Notebooks](#programs)
  - [Analytics](Analytics.ipynb)
  - [Joins and Unions Examples](Joins&nbsp;and&nbsp;Unions&nbsp;Examples.ipynb)
## Overview
This repository is a collection of Jupyter notebooks written in python to execute SQL queries against various tables in the Google BigQuery database.
## Client
#### Create `gcloud service-accounts` in active project
#### 2. `gcloud cli` commands
*   `gcloud iam service-accounts create [SA_NAME] 
    --description="[DESCRIPTION]" 
    --display-name="[DISPLAY_NAME]"` command to begin.
#### Grant BigQuery roles
#### Only grant privileges required for bigquery client role
*   `gcloud projects add-iam-policy-binding [PROJECT_ID] --member="serviceAccount:[SA_NAME]@[PROJECT_ID].iam.gserviceaccount.com" --role="roles/bigquery.user"`
*    `gcloud projects add-iam-policy-binding [PROJECT_ID] --member="serviceAccount:[SA_NAME]@[PROJECT_ID].iam.gserviceaccount.com" --role="roles/bigquery.dataViewer"`

#### Generate a Service Account key
*    `gcloud iam service-accounts keys create [KEY_FILE_NAME].json --iam-account=[SA_NAME]@[PROJECT_ID].iam.gserviceaccount.com`

