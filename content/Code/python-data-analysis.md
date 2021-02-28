---
title: "Making Sense of Your Data With Python"
date: 2021-02-22T20:25:19-08:00
draft: true
---

## About
---
Communication is a massive part of any good security program. Being able to demonstrate successes, failures, and areas of improvement for organizational security posture to the executive level is critical to receiving buy-in and resources from your business to mitigate risk in your environment effectively. If the business does not see the need for spending more time and money on security, they likely will turn their attention elsewhere.

One of the best methods for demonstrating security posture is to provide metrics from existing security controls, but this often easier said than done. Many security tools will allow you to visualize trends within themselves, and many will allow you to export data to spreadsheets, or provide APIs to pull data.

----
## Intro to Pandas

Pandas is a great tool for programmatically handling spreadsheets with Python. Pandas can easily convert formats like CSV, Excel, and Python Dictionaries to Pandas *DataFrames*. A Pandas DataFrame is a data structure that organizes data into rows and columns, and provides the flexibility to easily manipulate formatted data for analysis

### Working with DataFrames

**This section assumes that you have some knowledge of Python 3.x with topics like lists, dictionaries, and conditional statements.**

1. Install Pandas

	Use `pip install pandas` (or `pip3 install pandas` if Pip for Python 3.x is not set as your default Pip install)

2. Create your file and import Pandas
	Create a file, name it something like `analytics.py` or `csv-parsing.py`. Import Pandas by adding this line of code to the top of your file
	```python
	import pandas
	```

2. Create or upload your CSV File
	```
	intColumn,strColumn,dataColumn
	1,someData,2-28-2021
	3,someMoreData,3-13-2021
	5,someFinalData,1-18-2021
	```
3. Load your data into pandas
	```
	dataFrame = pandas.read_csv("example.csv")
	```
4. Your data is now loaded into a data frame that we can use for processing, the data frame can be visualized with the following table


intColumn (ints)| strColumn (strings) | dataColumn (datetime objects)
|---|---|---|
1 | someData | 2-28-2021
3 | someMoreData | 3-13-2021
5 | someFinalData | 1-18-2021