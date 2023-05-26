# spd-alpr
Analysis of Seattle Police Department Automated License Plate Reader. 

- [Descriptive analysis](https://uwchr.github.io/spd-alpr/)
- [Statistical analysis](https://uwchr.github.io/spd-alpr/analyze.html)

## About the data

Via public records request, the University of Washington Center for Human Rights (UWCHR) obtained one week of Seattle Police Department (SPD) Automated License Plate Reader (ALPR) data from 2021-10-01 to 2021-10-08. The data were released in two separate files, both PDF prints of Excel spreadsheet data:

- `ReadsSummaryReport-2021-12-28T17-40-44_768_DateTime_Redactions_Redacted.pdf`
- `ReadsSummaryReport-2021-12-28T17-40-44_768_Plate_Redactions_Redacted.pdf`

These files are identical, with the exception that in the first the date/time value of the ALPR read is redacted; while in the second ALPR read values are redacted. These files were converted to text format using `pdftotext` and further cleaned and converted to CSV format using R scripts. 

Because the files were identical with the exception of the redacted fields, it was trivial to join these files into one containing both plate read and date/time values. The validity of this join operation was confirmed using device read summary fields embedded in the data, as well as other features of the files. To protect privacy, these operations were performed in a private development repository and plate read values were encrypted prior to publication.
