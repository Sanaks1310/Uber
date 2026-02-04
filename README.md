# Uber Data Analytics: End-to-End Power BI Project 🚗

## Project Overview
This project focuses on analyzing Uber trip data to uncover patterns in rider behavior, peak demand hours, and supply-demand imbalances. By leveraging Power BI, I transformed raw trip records into a strategic dashboard that helps identify high-growth areas and optimize driver distribution.

## Key Features
Ride Volume Trends: Analysis of daily, weekly, and monthly trip frequencies.
Geospatial Visualization: Map-based analysis of pickup and drop-off hotspots.
Supply-Demand Gap: Identification of hours where "No Cars Available" or "Cancelled Trips" are highest.
Revenue Insights: Breakdown of total fares, surge pricing impacts, and average trip cost.

## Technical Stack
Tool: Power BI Desktop
Data Source: Uber Request Data (Kaggle / Trip Records)
Data Cleaning: Power Query (Advanced filtering & Date/Time splitting)
Analysis: DAX for complex time-intelligence and gap analysis

## Workflow
Data Extraction & Profiling: Handled datasets containing timestamps, locations, and trip statuses.
ETL Process (Power Query):
Split 'Timestamp' into Date and Hour for granular time analysis.
Handled null values in "Driver ID" (indicating unfulfilled requests).
Categorized "Hours" into Time Slots (Early Morning, Morning, Afternoon, etc.).
Data Modeling: Implemented a Star Schema with a dedicated Calendar table to enable time-intelligence features.
Calculated Measures (DAX): * Total Requests = COUNT(Uber[Request ID])
Completion Rate = DIVIDE([Completed Trips], [Total Requests], 0)
Demand Gap = [Total Requests] - [Completed Trips]
UI/UX Design: Used Uber’s signature black-and-white color palette for a professional, brand-aligned look.

## Business Insights
Peak Gap Periods: Discovered that the highest supply shortage occurs during evening rush hours in specific city sectors.
Cancellation Patterns: Identified that "Cancelled by Driver" is most frequent in the morning, while "No Cars Available" peaks at night.
Revenue Optimization: Highlighted high-distance routes that contribute most to the total fare revenue.

##How to Use
Clone this repository.
Open the Uber_Analysis.pbix file.
Ensure your Power BI version is updated to view all custom visuals.
