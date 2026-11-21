# Bike Lakehouse Project

## Project Overview

This project focuses on building a Data Lakehouse using Databricks.

The goal is to take raw bike-related data, clean and transform it, and prepare it for business analysis and reporting.

I used the **Medallion Architecture**, which organizes data into three layers:

**Bronze → Silver → Gold**

I also created a Databricks Job and pipeline to automate the execution of the notebooks. The job is scheduled to run every two days.

## Problem Statement

Raw data is not always ready for business analysis. It may contain duplicate records, missing values, inconsistent formats, and unorganized information.

Processing this data manually every time can also be time-consuming.

This project addresses these problems by:

- Organizing raw data into separate processing layers.
- Cleaning and standardizing data.
- Preparing structured, business-ready tables.
- Automating the data processing workflow using Databricks Jobs.
- Scheduling the pipeline to run every two days.

## Project Architecture

The project follows the Medallion Architecture.

### 1. Bronze Layer – Raw Data

The Bronze layer is the first layer.

In this layer, I:
- Loaded source CSV files into Databricks.
- Read the raw data.
- Created tables in the Bronze layer.
- Stored the original data without applying transformations.

**Purpose:** To maintain the raw source data for further processing.

### 2. Silver Layer – Data Cleaning and Transformation

The Silver layer is used to clean and prepare the data.

In this layer, I:
- Read data from Bronze tables.
- Checked data quality.
- Identified duplicate and missing values.
- Cleaned and standardized the data.
- Renamed columns where required.
- Transformed the data into a structured format.
- Saved the processed data into Silver tables.

**Purpose:** To make the data clean, consistent, and reliable.

### 3. Gold Layer – Business-Ready Data

The Gold layer is the final layer.

In this layer, I:
- Used the cleaned Silver data.
- Combined relevant tables.
- Organized the data based on business requirements.
- Created fact and dimension tables.
- Prepared structured data for analytics and reporting.

**Purpose:** To make the processed data ready for business analysis and reporting.

## Pipeline Automation

To avoid running the notebooks manually every time, I created a Databricks Job and pipeline.

- Organized the notebooks into different processing layers.
- Configured the job to execute the required tasks.
- Scheduled the job to run automatically every two days.

**Purpose:** To automate the data processing workflow and keep the processed data updated on a regular schedule.

## Tools and Technologies

- **Databricks:** Used for building and processing the Lakehouse.
- **Unity Catalog:** Used to organize the Bronze, Silver, and Gold schemas.
- **Databricks Jobs and Pipelines:** Used to schedule and automate notebook execution.
- **GitHub:** Used to store and manage project notebooks and files.

## Project Structure

```text
databricks_project/
│
├── datasets/
│      
└── scripts/
    │
    ├── bronze/
    │
    ├── silver/
    │
    └── gold/
```

## What I Learned

Through this project, I gained practical experience in:

- Understanding Data Lakehouse architecture.
- Working with Medallion Architecture.
- Organizing data into Bronze, Silver, and Gold layers.
- Loading raw data into tables.
- Data cleaning and transformation.
- Understanding fact and dimension tables.
- Creating Databricks Jobs and pipelines.
- Scheduling automated data processing.
- Connecting Databricks with GitHub.

## Project Outcome

The project provides an organized and automated data processing workflow.

Raw bike-related data is loaded into the Bronze layer, cleaned and transformed in the Silver layer, and structured into business-ready tables in the Gold layer.

The Databricks Job runs every two days, helping automate the workflow and reduce manual execution.
