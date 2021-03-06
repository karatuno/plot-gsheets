# plot-gsheets
plot-gsheets is a small wrapper around the Google Sheets API (v4) to provide more convenient way to plot Google Sheets from Python scripts.

## Links
1. Github: https://github.com/karatuno/plot-gsheets
2. PyPi: https://pypi.org/project/plot-gsheets/

## Installation
This package runs under 3.5+, use [pip](https://pip.pypa.io/en/stable/) to install:
```bash
pip install plot-gsheets
```
## Usage
#### Importing plot_gsheets
```python
>>> import plot_gsheets
```
### Get all columns of google sheet
Syntax:
```python
plot_gsheets.get_columns(SPREADSHEET_ID,sheet_name)
```
where **SPREADSHEET_ID** can be found like here in you google sheet URL:

https://docs.google.com/spreadsheets/d/SPREADSHEET_ID/edit#gid=0

and **sheet_name** can be found at the bottom left of window 

[![2Ueaix.th.png](https://iili.io/2Ueaix.th.png)](https://freeimage.host/i/2Ueaix)

example:
```python
>>> plot_gsheets.get_columns('1SrZfvr2ee54r7HR1jGtAE9zHIj_Y-UzK9ok8bdwkpqc','Sheet1')
['timestamp', 'average_sales', 'offer_price']
```

### Plot by specifying columns

Syntax:
```python
plot_gsheets.plot_sheet_columns(SPREADSHEET_ID,sheet_name,x_column_name,y_column_name)
```
sheet columns can be found by using **plot_gsheets.get_columns** and thus **x_column_name,y_column_name** can be specified by seeing output

example :
```python
>>> plot_gsheets.plot_sheet_columns('1SrZfvr2ee54r7HR1jGtAE9zHIj_Y-UzK9ok8bdwkpqc','Sheet1','timestamp','average_sales')
```
[![2UetJS.png](https://iili.io/2UetJS.png)](https://freeimage.host/)

plot will be saved as **plot.png**

### Google colab example :

https://colab.research.google.com/drive/1yIW8wunsHVJiwRKltNQ7fBi9ph37Xqu2?usp=sharing
