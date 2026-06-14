# dbt-fundamentals

## Project Overview
This repository contains a dbt (data build tool) project focused on the core fundamentals of analytics engineering. It implements the classic Jaffle Shop and Stripe ecommerce datasets to demonstrate modular data modeling, testing, documentation, and staging/marts architectures.

## Tech Stack
- **Data Transformation Tool**: dbt (data build tool) Core
- **Database Backend**: Snowflake / DuckDB / BigQuery (configured via profiles)
- **Languages**: SQL, Jinja templating, YAML (configuration and schemas)

## Key Implementation Details
- **Project Structure**:
  - **Staging Layer (`models/staging`)**: Cleans, casts, and prepares raw source tables (`jaffle_shop` and `stripe`) for downstream modeling.
  - **Marts Layer (`models/marts`)**: Constructs dimensional models (e.g., customers, orders, and payments) ready for business intelligence and reporting.
- **Custom Macros & Testing**:
  - Utilizes reusable SQL snippets with Jinja macros.
  - Implements schema tests (uniqueness, non-null, accepted values, referential integrity) and documentation inside YAML files.
- **Seeds & Snapshots**:
  - Incorporates seed files for static lookup data.
  - Utilizes snapshots for tracking changes over time (SCD Type 2).
