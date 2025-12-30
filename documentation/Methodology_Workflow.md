# Methodology & Workflow

This project followed a structured analytical workflow to transform raw financial data into a decision-ready executive dashboard.

## 1. Data Import and Transformation
- Connected Excel to raw source files using **Power Query**.
- Removed unnecessary top rows and promoted headers across all tables.
- For the **Category Mapping** table, headers were manually adjusted due to structural inconsistencies.
- All cleaned tables were loaded into the **Power Pivot data model**.

## 2. Data Modeling
- Implemented a **star schema** with the following core tables:
  - `Calendar`
  - `Actuals_Data`
  - `Budget_Data`
  - `CostCenters`
  - `CategoryMapping`
- Built relationships using shared fields such as:
  - `Date`
  - `Cost Center`
  - `Department`
  - `Category`
- Addressed language inconsistencies between English and Spanish month names by:
  - Creating translated month columns
  - Building a synthetic date column for Budget data

## 3. DAX Measures and Calculations
Core financial measures were created to support variance analysis and performance tracking:

- `Total Cost` — SUM of actual expenses  
- `Total Budgeted Cost` — SUM of planned amounts  
- `Variance` — Actual minus Budget  
- `Variance %` — Variance divided by Budget  
- Accumulated monthly measures for **year-to-date (YTD)** tracking

## 4. Visualization and Dashboard Design
- Built multiple **Pivot Tables** as data sources for visuals.
- Designed and formatted key visuals:
  - Line chart showing accumulated **Budget vs Actual**
  - Bar chart for **variance by department**
  - **Top 5 variance by category** with conditional formatting
  - Variance analysis by region
- Added dynamic **slicers** for region, department, and month to enable interactive analysis.

## 5. Design Iteration and Refinement
- Added visual indicators (icons) to highlight positive and negative variances.
- Improved overall layout and user experience for executive readability.
- Resolved filtering issues caused by missing or incorrect relationships.
- Replaced legacy visuals with clearer and more intuitive bar and line charts.
