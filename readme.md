# Surfline Dashboard

## **Architecture**


<img width="4896" alt="Surfline App Architecture" src="https://user-images.githubusercontent.com/5299312/169568492-4ada773b-a77b-485e-9c2e-b4538017ef59.png">


## **Overview**

The pipeline collects data from the surfline API and exports a csv file to S3. Then the most recent file in S3 is downloaded to be ingested into the Postgres datawarehouse. A temp table is created and then the unique rows are inserted into the data tables. Airflow is used for orchestration and hosted locally with docker-compose and mysql. Postgres is also running locally in a docker container. The data dashboard is run locally with ploty.

## **ETL** 

![image](https://user-images.githubusercontent.com/5299312/169564659-76d6cde9-fc59-4d18-9fc4-d8d6f8fa1c0b.png)

## **Data Warehouse - Postgres**

![image](https://user-images.githubusercontent.com/5299312/169566679-3d46d244-b139-4414-a406-c5c18d981ac3.png)

## **Data Dashboard**

![image](https://user-images.githubusercontent.com/5299312/169568656-e6a77014-4bd2-4d21-9236-f24d6f1061b7.png)

