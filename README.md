# tbta-csv

> ! NOTE: this repository has been superseded by Kevin Edey's work, [tbta_db_export](https://github.com/AllTheWord/tbta_db_export).

A CSV dump of The Bible Translator's Assistant data

If you use this data, please share a pull request to the README or message me to add a link to what you're doing with it. Thanks!

## What is this?

This is a CSV dump of the data from The Bible Translator's Assistant (TBTA) project. The data is in the form of a CSV file, with each row representing a single word. Each table in the original Access databases is contained in a separate CSV file.

## What is TBTA?

The Bible Translator's Assistant (TBTA) is a project to create a database of Bible words in all languages of the world. Read more at their [website](https://alltheword.org/our-downloads/).

## What is the license?

Todd Allmann and Richard Denton confirmed on April 13, 2023 in a Missional AI 2023 Zoom session that the data may be freely distributed.

## Regenerate/Update the CSV files

If a new release is made available, you can regenerate the CSV files by running the script contained in the `source/export-access-db-to-csv.ipynb` notebook. You will need to install the `pyodbc` package to run the script using `pip install pyodbc`.

Please note the first code block:
```python
# NOTE: update this path to your downloaded TBTA data dump
mdb_folder_path = "/path/to/Bible-Ontology-English-May-12-2022/"

# NOTE: you will need the mdbtools package installed on your system
# On MAC, you can install it in your Terminal app with homebrew: `brew install mdbtools`

# Check the binary location in Terminal using `which mdb-export` and copy the path here
mdb_export_binary = "/opt/homebrew/bin/mdb-export"  # Change this path to the one found on your system
```

Essentially, you will need to download the TBTA data dump from their [website](https://alltheword.org/our-downloads/), and then update the `mdb_folder_path` variable to point to the folder containing the `.mdb` files. You will also need to install the `mdbtools` package on your system, and then update the `mdb_export_binary` variable to point to the binary location of the `mdb-export` command.
