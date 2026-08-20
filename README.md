# SpaceX Launch Schedule Web Scraping

This project builds a Python data-acquisition workflow that extracts SpaceX launch information from a public schedule page, structures the results with pandas, exports a reusable CSV, and presents the data in Tableau.

## Objective

Convert semi-structured launch listings into a tabular dataset containing mission, vehicle, provider, location, date, time, description, and mission-tag fields.

## Tools and Technologies

- Python
- `requests` and Beautiful Soup
- pandas and Python datetime utilities
- Jupyter Notebook
- Tableau Public

## Workflow

1. Request the SpaceX-filtered schedule page from RocketLaunch.Live.
2. Parse each launch card with Beautiful Soup selectors.
3. Handle missing fields and alternate date/time representations.
4. Store the extracted records in a pandas DataFrame.
5. Normalize the date field and export the result to CSV.
6. Use Tableau Public to explore missions and launch dates interactively.

## Key Results and What This Demonstrates

- The saved dataset contains 26 launch records and eight structured fields.
- The notebook demonstrates HTTP requests, defensive HTML extraction, missing-value handling, date parsing, tabular export, and visualization handoff.
- The project illustrates how a web page can be converted into analysis-ready data while keeping acquisition and presentation steps distinct.

The CSV is a point-in-time snapshot. Launch schedules and page structure can change, so the scraper may require selector maintenance when rerun.

## Visualization

[View the interactive Tableau story](https://public.tableau.com/app/profile/david.salgado4874/viz/SpaceXlaunchdates/Story1)

## Repository Contents

| Path | Description |
| --- | --- |
| [`Webscraping.ipynb`](Webscraping.ipynb) | Scraping, parsing, cleaning, and CSV-export workflow |
| [`spacex_launch_schedule.csv`](spacex_launch_schedule.csv) | Saved structured launch-schedule snapshot |

## Data Source and Viewing

- [RocketLaunch.Live SpaceX schedule](https://www.rocketlaunch.live/?filter=spacex)
- [View the notebook in nbviewer](https://nbviewer.org/github/Salgadod123/Webscraping-Project/blob/main/Webscraping.ipynb)

This project uses a single page request and is intended as a small portfolio demonstration, not a high-frequency collection system.
