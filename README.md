# Lynching Data from Ida B. Wells' Red Record, 1893 and 1894
## Sourcing and Files
This project forks a project by an IUP student which scraped **lynching data** out of Ida B. Wells' *Red Record*. Their data was concatenated into one excel file, which is manipulated by red_record.rmd. The R Markdown file takes city and state (with the help of state_abbrev.xlsx) and runs it hrough Google's Maps API to get latitude and longitude data, which is then added onto the dataframe. The resultant data is exported to red_record_states.xlsx. The xlsx file is exported to csv for use testing a sqlite database. The xlsx file is exported to a geojson file using online tools, and this red-record-states.geojson is our main file of importance.

## Automation
The Git repo for this project uses build_script.sh to **automatically update a datasette website** displaying the data in red-record-states.geojson every time the file is pushed to the repo with changes. The logs for this automatic process are stored in build_log. 

## Purpose
This project is testing datasette capability for an upcoming investigation by the **Howard Center for Investigative Journalism**.
