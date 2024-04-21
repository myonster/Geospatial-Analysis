# Geospatial Analysis Project

## Project Overview
This project analyzes geospatial data from New York City and constructs predictive models. The dataset provides information on mobile devices' speed, altitude, and coordinates over a 14-day period, enabling insights into urban mobility and device usage patterns.

## Dataset
The dataset, "New York City Geospatial dataset," contains data recorded from February 8, 2020, to February 21, 2020. Each entry comprises:

| S No. | Column Name         | Data Type             | Description |
|-------|---------------------|-----------------------|-------------|
| 1     | advertiser_id       | Categorical (Integer) | Unique identifier for the mobile device (0-49) |
| 2     | platform            | Categorical (Integer) | Android (0) or iOS (1) |
| 3     | location_at         | Integer               | UTC timestamp of the observation |
| 4     | latitude            | Floating point        | Latitude of the observation in decimal degrees |
| 5     | longitude           | Floating point        | Longitude of the observation in decimal degrees |
| 6     | altitude            | Floating point        | Altitude in meters above/below sea level |
| 7     | horizontal_accuracy | Floating point        | Horizontal accuracy in meters |
| 8     | vertical_accuracy   | Floating point        | Vertical accuracy in meters |
| 9     | speed               | Floating point        | Speed in meters/second |
| 10    | publisher_id        | Categorical (Integer) | ID of the publisher app (0-7) |
| 11    | model               | Categorical (Integer) | Device model category (0-28) |
| 12    | day                 | Categorical (Integer) | Day number of data collection (1 corresponding to February 8th) |

## Jupyter Notebooks
### 1. `geospatial_data.ipynb`
This notebook is designed to process and visualize complex geospatial data. Key functionalities include:
- **Data Loading**: Importing data from a CSV file and handling potential data type inconsistencies.
- **Data Processing**: Converting UNIX timestamps to human-readable date-time formats, calculating distances using geospatial coordinates, and deriving travel speeds.
- **State Analysis**: Categorizing device movements into states such as walking, transit, or stationary based on speed and altitude data.
- **Visualization**: Using Folium for mapping trajectories, displaying speed and state changes over geographic maps, and integrating time-based data overlays to provide insights into temporal patterns.

### 2. `predictive_model.ipynb`
This notebook focuses on predictive analytics using machine learning techniques to understand device behavior and movement trends. It features:
- **Data Cleaning and Transformation**: Standardizing data, handling missing values, and encoding categorical variables.
- **Clustering for Speed Analysis**: Applying K-means to group data points into clusters based on speed to identify areas of different traffic conditions.
- **Platform Prediction**: Using classifiers like Logistic Regression and Decision Trees to predict the operating system of the device based on location accuracy metrics.
- **Geospatial Prediction**: Developing regression models to forecast future locations based on historical data patterns, employing algorithms such as Neural Networks and K-Nearest Neighbors for spatial prediction.

## Installation
Python environment with the necessary libraries:

### Requirements
- Python 3.6 or higher
- Jupyter Notebook
- Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn, tensorflow, geopandas, folium

### Setup
Clone the repository and install dependencies:

```bash
git clone https://your-repository-url.git
cd your-repository-directory
pip install -r requirements.txt
