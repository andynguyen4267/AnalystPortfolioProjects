# COVID-19 SQL Data Exploration and Analysis Project

This project explores and analyzes global COVID-19 data using Microsoft SQL Server Management Studio (SSMS). It involves extracting insights from two datasets: `CovidDeaths` and `CovidVaccinations`. The focus is on trends in infections, deaths, and vaccination efforts, with calculations and aggregations to derive meaningful public health metrics.

---

## Datasets Used

- `CovidDeaths`
- `CovidVaccinations`

These datasets include country-level information on daily COVID-19 cases, deaths, population, and vaccinations.

---

## Skills Demonstrated

- SQL Joins
- Aggregations with `SUM`, `MAX`, `COUNT`
- Window Functions (`OVER`, `PARTITION BY`, `ORDER BY`)
- Common Table Expressions (CTEs)
- Temporary Tables
- Creating SQL Views
- Filtering with `WHERE`, `LIKE`, and `IS NOT NULL`
- Calculated Columns and Percentages

---

## Key Analyses Performed

### Basic Exploration
- Selected starting data from the `CovidDeaths` table
- Filtered out invalid entries (e.g. rows where `continent` is null)

### Death Rates
- Calculated the death percentage by comparing `total_deaths` to `total_cases` for each country
- Focused analysis on the United States

### Infection Rates
- Computed the percentage of each country's population infected with COVID-19
- Identified countries with the highest infection rates

### Highest Death Counts
- Ranked countries by total death counts
- Aggregated and ranked continents by total deaths

### Global Summary
- Summed up new cases and new deaths across the world
- Calculated the global death rate

### Vaccination Analysis
- Joined the `CovidDeaths` and `CovidVaccinations` tables
- Used window functions to calculate a rolling sum of vaccinated individuals per country
- Computed the percentage of population vaccinated over time

---

## Tableau Dashboard

[**View Interactive Dashboard on Tableau Public**](https://public.tableau.com/app/profile/andy.nguyen4739/viz/CovidDashboardProject_17520765885390/Dashboard1)  

---

## Techniques Used

### Common Table Expression (CTE)
Used a CTE named `PopvsVac` to simplify and reuse vaccination-related calculations.

### Temporary Table
Created a temporary table `#PercentPopulationVaccinated` to store rolling vaccination data and compute percentages.

### SQL View
Created a view `PercentPopulationVaccinated` for easy access to cleaned and prepared data for future visualizations.
