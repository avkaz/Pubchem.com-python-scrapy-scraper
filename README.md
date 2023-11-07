# Web Scraping Project Readme

## Project Overview

This web scraping project has been designed to extract data from the website 'https://pubchem.ncbi.nlm.nih.gov/ptable'. The goal is to crawl the chemical elements table and collect information about each element, including their symbol, name, atomic number, atomic mass, and chemical group. To accomplish this, Scrapy, a powerful web scraping framework, is used in combination with Scrapy-Playwright to interact with the website, as it utilizes JavaScript to display content.

## Project Structure

The project consists of the following components:

1. **Scrapy Spider**: The main web scraping component responsible for crawling the target website and extracting the required data. The spider is configured to use Scrapy-Playwright to handle JavaScript rendering.

2. **`items.py`**: Defines the structure of the items that the spider will yield. This file specifies the format in which the scraped data will be stored.

3. **Pipelines**:
   - **Database Upload Pipeline**: This pipeline is responsible for uploading the scraped data to a database. You need to configure the database connection settings in the settings.py file.
   - **JSON Export Pipeline**: This pipeline is used to divide all the elements into groups and save the data in JSON format. You can customize the grouping logic based on your requirements.

4. **Settings**: The settings file contains configuration options for the Scrapy project, including settings for pipelines, middleware, and user-agent.
