## Project Overview
This project investigates the relationship between the quality of state-level Open Data portals and new business formation rates (specifically High-Propensity Business Applications) across US states from 2005 to 2024.
By utilizing Natural Language Processing (Hugging Face Transformers) to semantically analyze metadata from government portals, and combining this with economic indicators (GDP, Population) and Business Formation Statistics (BFS), the project aims to quantify the economic value of public data accessibility.

## Features
- **Multi-Platform Data Harvesting:** hybrid scraping/API strategy to fetch metadata from ArcGIS Hub, Socrata, and CKAN portals.
- **Semantic Analysis:** Uses a pre-trained `gpt2` model to embed dataset descriptions and calculate cosine similarity against a "Business/Finance" context vector.
- **Panel Data Construction:** Merges unstructured portal metadata with structured economic time-series data.
- **Econometric Modeling:** Implements a Fixed Effects Regression model (State and Year Fixed Effects) to estimate elasticity.
- **Visualization:** Generates 2D trend lines and 3D trajectory plots to visualize the evolution of data quality and business growth.

## Data Sources
- Open Data Portals: Scraped dynamically from US states domains (e.g., data.ca.gov, data.texas.gov).
- Business Formation Statistics (BFS): US Census Bureau (CSV required).
- GDP by State: Bureau of Economic Analysis (CSV required).
- Population: US Census Bureau API (Fetched dynamically).

## Usage
Ensure BFS-mf.csv and the GDP CSV file are in the project root.
Insert your Census API key in the __main__ section of main.py if necessary (a default key is "bcdbdffc30535ef4f01e36911b44e69562920953").
Run the script:
