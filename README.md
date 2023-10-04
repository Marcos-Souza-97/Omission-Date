# Omission-Date
Calculate the number of omissions of ships in Brazilian ports.

The code provided is a part of a system that deals with the calculation of expected dates for omission of container vessels in Brazilian ports based on information from shipowners' schedules. It automates the process of calculating these target dates and updating them in an Excel spreadsheet. Here is a summary of the code:

Importing libraries:

The code starts by importing the pandas and datetime libraries to handle data and date manipulation operations.
Uploading the Excel spreadsheet:

It loads an Excel spreadsheet named 'BASE.xlsx' located in a specific path on the computer.
Obtaining the date column:

It extracts the 'DATE' column from the loaded spreadsheet.
Converting strings to datetime objects:

The dates present in the column are converted from strings to datetime objects so that they can be manipulated easily.
Filling empty cells:

The code goes through the date column and checks if a date is missing (empty cell).
If a cell is empty, it calculates a new date by adding 3 days to the date in the previous row.
If the new date results in a different month, the date is adjusted to the first day of that new month.
This logic ensures that the dates scheduled for omission follow a sequence of three days and do not exceed the month.
Conversion back to strings:

After the forecast dates are calculated, they are converted back to string format in the format 'YYYY-MM-DD'.
Update the date column in the spreadsheet:

The calculated target dates are assigned to the 'Date' column in the original spreadsheet.
Saving changes to the spreadsheet:

Changes made to the spreadsheet are saved in the same 'BASE.xlsx' file, replacing the original file.
In short, this code automates the process of calculating the expected dates for the omission of vessels in Brazilian ports, ensuring that these dates follow a consistent logic of three days between each omission and do not exceed the limits of the months. This facilitates the generation of reports and analyzes related to the number of omissions for each port per month.
