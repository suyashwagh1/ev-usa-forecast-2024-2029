EV Market Forecasting & Growth Analysis

A data science project analyzing Electric Vehicle (EV) adoption trends across the United States and forecasting future registrations through 2029 using exponential growth modeling.


Project Overview

This project performs end-to-end exploratory data analysis on 177,000+ EV registration records and builds a forecasting model using SciPy curve fitting to project EV market growth from 57K registrations (2023) to 627K+ by 2029.


Table of Contents


Dataset
Tech Stack
Project Structure
Key Analysis
Forecasting Model
Results
How to Run



Dataset


Source: Electric Vehicle Population Data (Washington State)
Size: 177,866 records
Features: VIN, County, City, State, Model Year, Make, Model, Electric Vehicle Type, Electric Range, Base MSRP, and more



Tech Stack

ToolPurposePythonCore programming languagePandasData manipulation and cleaningNumPyNumerical computationsMatplotlibData visualizationSeabornStatistical visualizationsSciPyExponential growth curve fitting

Key Analysis

1. EV Registrations by Model Year


Tracked EV adoption growth from 1997 to 2023
Identified exponential growth trend post-2018
2023 recorded the highest registrations at 57,519 vehicles


2. Electric Range Distribution


Analyzed range distribution across all EV models
Calculated mean electric range across the dataset
Tracked improvement in average range by model year


3. Top Cities & Manufacturers


Identified Top 20 cities by EV registration count
Analyzed Top 10 EV models by average electric range
Compared performance across leading manufacturers



Forecasting Model

Used exponential growth modeling via SciPy's curve_fit function:

pythonfrom scipy.optimize import curve_fit

def exp_growth(x, a, b):
    return a * np.exp(b * x)

params, covariance = curve_fit(exp_growth, x_data, y_data)


Trained on historical data from 1997–2023
Forecasted registrations for 2024–2029



Results

YearForecasted EV Registrations202479,0792025119,6542026181,0472027273,9412028414,4972029627,171

Key finding: EV registrations projected to grow 10x from 2023 to 2029, reflecting strong long-term market expansion.
