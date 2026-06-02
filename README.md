# Fleet-Management-Dashboard-in-Power-BI
Project Overview

Fleet Overview Dashboard is a Business Intelligence solution designed to monitor fleet performance, fuel costs, operational efficiency, and environmental impact.

The dashboard provides decision-makers with a consolidated view of key transportation metrics, including parcel volume, fuel consumption, transportation costs, CO₂ emissions, and vehicle utilization.

Data Source

The data used in this project is automatically collected from an external Fuel Price API.

A Python ETL process runs on a daily schedule and retrieves the latest fuel prices for multiple fuel types.

The API returns information such as Date, Fuel type, Price

You can find the Python code on my GitHub in the Vehicle-Fuel-Cost-Report repository.
The collected data is automatically stored and refreshed every day, ensuring that the Power BI report always uses up-to-date fuel price information.

Data Processing

The daily API data is processed using Python and prepared for analytical reporting.

The ETL pipeline performs the following steps:

Connects to the fuel price API.
Retrieves current fuel prices.
Stores historical records by date and fuel type.
Cleans and validates incoming data.
Exports the processed dataset for Power BI consumption.
Cost Calculation Logic

To avoid daily fuel price fluctuations affecting operational KPIs, fuel costs are calculated using a rolling 7-day average fuel price.

For each fuel type, Power BI calculates:

Average Fuel Price (Last 7 Days)

This value is then multiplied by the actual fuel consumption recorded for a specific vehicle category or operational activity.

Calculation logic:

Fuel Cost = Fuel Consumption (L) × 7-Day Average Fuel Price

This approach provides more stable and representative cost indicators while reducing the impact of short-term market volatility.

Key Performance Indicators

The dashboard includes the following KPIs:

Parcel Volume
Fuel Cost
Distance Travelled
Fuel Cost per Parcel
Fuel Consumption per Parcel
Load Utilization
Carbon Emissions per Parcel
Analytical Views

The report enables users to analyze:

Fuel costs over time
Fuel cost per parcel trends
Fuel cost by vehicle type
Fuel cost by fuel type
Regional fleet performance
Vehicle utilization
CO₂ emissions
Technology Stack
Python
Pandas
REST API
Power BI
DAX
Power Query
Automated Refresh

The entire solution is designed as an automated reporting pipeline.

Every day:

Python retrieves new fuel price data from the API.
Historical fuel price tables are updated.
Power BI refreshes the dataset.
KPIs and visualizations are recalculated automatically.

This ensures that fleet managers and business users always have access to the latest operational and fuel cost information.

Business Value

The dashboard supports data-driven decisions related to:

Fuel cost optimization
Fleet efficiency monitoring
Transportation cost control
Sustainability and CO₂ reporting
Regional performance benchmarking

By combining operational fleet data with automatically refreshed fuel market information, the solution provides a comprehensive view of transportation performance and cost drivers.
