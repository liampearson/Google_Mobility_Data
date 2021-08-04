# Google_Mobility_Data

Google has started releasing mobility reports in response to the COVID-19 pandemic. In the essence of transparency they have provided the **datasets**!

I built this code to assist www.covid19data.com.au <-- a leading publisher of covid19 data in Australia made by Juliette O'Brien (@juliette_io)

In its current form, this code is quite bespoke in that it writes to specific spreadsheets in specific drives.

## The Data
For each Region (Country) there are the following categories (separate csvs):
- retail_and_recreation_percent_change_from_baseline
- grocery_and_pharmacy_percent_change_from_baseline
- parks_percent_change_from_baseline
- transit_stations_percent_change_from_baseline
- workplaces_percent_change_from_baseline
- residential_percent_change_from_baseline


Since covid19data.com.au uses a lot of google functionality, this code is built to run on Google Colab (but can be run locally)

## Process
1. Login/Provide access between colab and Google Drive
2. Provide access between colab and Google Sheets
3. Download the zip file (uploaded daily but with a ~4day lag)
5. Unzip the files
6. Get AU (Australia) data for both 2020 and 2021 (you can modify this to get your region)
7. Create a dictionary of STATE/LGA names and the unique identifier used by google
8. For each category, get the daya, transpose it and write it to a google sheet
