# Complaint Data Cleaning Scripts

### Overview
In this directory are data cleaning scripts that clean FOIA-requested complaint files. Each subdirectory (e.g., complaints-cpd-2016-dec_copy_20170112) contains data files received in a different FOIA request. The month in the subdirectory name refers to the date the FOIA request was submitted.  Note that each FOIA request can have multiple reports in it that contain different data; each report is processed as necessary.
Note, 

### What data cleaning scripts in src do
1. **complaints-cpd-2016-dec_copy_20170112/complaints-cpd-2016-dec_import.ipynb** will
    - import location code dictionary
    - drop NAs in location code data
    - convert location codes to integer
    - *add 0s to location strings*
    - replace spaces with underscores in file names
    - rename columns & output to CSV
    - *reset index*
    - replace dashes with empty strings
    - convert address columns to single columns
    - rename columns
    - append location code    
    - creates a metadata table that contains
        - non-null counts
        - object types
        - unique counts
    - output data and metadata to CSV

2. **complaints-cpd-2016-jun_copy_20170112/complaints-cpd-2016-jun_import.ipynb** will
    - apply much of the same cleaning as as Dec 2016, but with additional processing
    - unlock locked files
    - skip first set of rows (header info)
    - make sure the file contains foia file/dates
    - drop null columns and NAs
    - drop rows where all date entries are NAs
    - fill number columns as needed
    - creates a metadata table that contains
        - non-null counts
        - object types
        - unique counts
    - output data and metadata to CSV
