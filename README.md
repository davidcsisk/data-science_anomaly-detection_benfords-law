# Benford's Law
An example of Anomaly Detection in accounting transactions using Benford's Law.

## Implemented as per:

* "The Use of Benford's Law as an Aid in Analytical Procedures" (Mark J. Nigrini and Linda J. Mittermaier)
* "Using Digital Frequencies to Detect Anomalies in Receivables and Payables" (Fabio Ciaponi, Francesca Mandanici)

## CONTENTS
* benfords_law.py - source code
* transactions_real.csv - list of transactions we'd like to check for anomalies 
* transactions_to_investigate.csv - table of transactions (and associated rules) that violate Benford's Law at the specified alpha level
* first_digit_plot.png, second_digit_plot.png - Expected vs. Observed frequency plots

## ORIGINAL AUTHOR
https://github.com/gbushnell/benfords_law

## HOW-TO
At the moment, the datafile name and the alpha value are hard-coded in the script. My first task is to make those arguments that can be 
passed in.

* To try it, simply execute the script like so:  python benfords_law.py
* The script will use the large CSV file as it's input of transactions, the produce the output CSV file with txns to check, plus the plots.

To make this potentially useful in practice, it may be worthwhile to include an ID column to tie back to the original transactions, 
and simply ignore that "primary key" column for computational purposes.

## ENHANCEMENTS

Done: 
* Add support for passing in arguments for CSV input filename and desired alpha level.  (Filename and alpha were hard-coded in original.)
* Added built-in help text when calling the script with no arguments.
* Build output filename from the input filename.

ToDo: 
*Add support for ID column(s) after the values to fit to the probability distribution to tie back to extracted txns.
	  