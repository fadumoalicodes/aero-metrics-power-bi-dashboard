# Aero-Metrics: Airport Commerical and Passenger Experience Dashboard

## Project Overview

Aero-Metrics is an end-to-end Power BI project analysing 199K flight records to uncover insights into operational performance, estimated passenger revenue and passenger feedback. The project demonstrates data cleaning with Power Query, relational data modelling, DAX calculations and interactive dashboard design.

## Dashboard Pages

### Flight Operations Overview

![Flight Operations Overview](images/flight-operations-overview.png)

### Commercial Insights

![Commercial Insights](images/commercial-insights.png)

### Passenger Feedback Insights

!passenger-feedback-insights.png!

## Tools and Skills

- Power BI
- Power Query
- DAX
- Relational data modelling
- Data cleaning and validation
- Fact and dimension tables
- Tooltips and drill-down
- Data visualisation and business analysis

## Data Model

The model contains the following relational tables:

- Flights fact
- Passenger feedback fact
- Weather fact
- Airlines dimension
- Routes dimension
- Origin airports dimension
- Destination airports dimension

Separate origin and destination airport dimensions were used to analyse both sides of each route without creating ambiguous relationships.

## Data Cleaning

The main data-cleaning tasks included:

- Removing duplicate flight records
- Converting scheduled and actual timestamps to Date/Time
- Replacing text-based null values with genuine nulls
- Standardising flight statuses and terminal values
- Correcting inconsistent airline names and country values
- Identifying passenger numbers exceeding aircraft capacity
- Checking invalid arrival and departure sequences
- Validating airline, route and airport foreign keys
- Correcting invalid destination airport codes through relational matching
- Removing or correcting invalid passenger-feedback records
- Treating negative visibility values as missing

## DAX Measures

The dashboard uses measures including:

- Total Flights
- Non-Cancelled Flights
- On-Time Rate
- Cancellation Rate
- Estimated Passenger Revenue
- Average Estimated Revenue per Flight
- Total Feedback Responses
- Passenger Recommendation Rate
- Estimated Passenger Feedback Rate

DAX functions used include:

`DISTINCTCOUNT`, `SUM`, `AVERAGE`, `CALCULATE`, `DIVIDE`, `FILTER`, `SUMX` and `AVERAGEX`.

Estimated passenger revenue was calculated by multiplying passenger numbers by the average fare for each non-cancelled flight.

## Key Findings

- The cleaned dataset contains approximately **199K flights**.
- The overall cancellation rate was approximately **14.4%**.
- The on-time arrival rate was approximately **43.7%**, using arrival within 15 minutes as the on-time threshold.
- Estimated passenger revenue was approximately **£9.1 billion**.
- The United Kingdom was the largest destination market, generating approximately **£3.6 billion** in estimated passenger revenue.
- Average estimated revenue per flight was approximately **£53.6K**.
- Approximately **50.2% of feedback respondents** said they would recommend the service.
- Feedback was received from an estimated **0.13% of passengers on non-cancelled flights**.

## Business Recommendations

1. **Improve operational reliability:** Investigate the drivers of the low on-time rate and prioritise airlines, airports and routes with the highest cancellation and delay levels.
2. **Protect high-value markets:** Maintain service quality and capacity across the highest-revenue destinations while assessing commercial performance alongside reliability.
3. **Increase feedback participation:** Introduce short automated post-flight surveys or QR codes to obtain more representative passenger insights.

## Dashboard Interactivity

- Tooltips provide additional flight, passenger and fare information.
- Users can drill from destination country to destination airport.
- Users can drill from origin airport to individual routes.
- The operations chart supports year-to-month drill-down.

## How to View the Dashboard

1. Download the `.pbix` file.
2. Open it in Microsoft Power BI Desktop.
3. Navigate through the three dashboard pages.
4. Hover over visuals to view tooltips.
5. Use the drill-down controls to explore the data.
