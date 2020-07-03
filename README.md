# covid-dashboard

Demo Link: `https://sz-test-279001.uc.r.appspot.com`

Demo Link 2: `https://velvety-tube-281911.el.r.appspot.com/`


## Running the code

1. Ensure you have python3 installed
2. Install the dependencies using `pip install -r requirements.txt`
3. Run the program using `python3 main.py`
4. Visit the page in your browser at `127.0.0.1:8080`

## Overview

This code reads saved versions of a google sheet in order to generate plots. It assumes that the data it needs is in the `static/data` folder. Namely, there are two files we expect:
1. `static/data/raw.csv`
2. `static/data/Sector-based Summary.json`

The first file is a csv dump of the google sheet, in particular the raw data tab. Google allows you to download this programitcally by hitting their api with a url like:
`https://docs.google.com/spreadsheets/d/<YOUR GOOGLE SHEET CODE >/gviz/tq?tqx=out:csv&sheet=Raw%20Data`.

Additionally, if you see in the example file `download_data.py`, you can programitally download json for all of the tables in a google sheet, one of which is named `Sector-based Summary.json`.

You will want to keep these cached somewhere, and update them here and there when the data changes, as google will rate limit you.

## Organization of Code
There are no tests yet, I haven't had time. The main driver of the code is in `main.py`. By default, it runs a server on `8080` in debug mode. This should be changed.