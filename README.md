# Threshold
Python tool to assess data for single-parameter thresholds

## Requirements
- python 3
- numpy
- matplotlib
- pandas
- scipy
- sklearn

## Contents
1. Imports
2. Read Data
3. Select Data
4. Threshold Analysis

## Recommended usage
- generate a csv file with IDs and experimental results (exp_example.csv)
- generate an excel sheet with IDs and computed features (comp_example.csv)
- put input files and jupyter notebook in same folder
- run jupyter notebook
	1. Imports
		- run imports cell to import required python packages
	2. Read Data
		- edit file names to match comp. and exp. input files and run cell
			(lines 1, 4, (and 5))
	3. Select Data
		- set dataset to read from experimental results and run cell
			(line 2)
	4. Threshold Analysis
		- set threshold settings 
			line 2, y_cut sets the experimental output cutoff
			line 3, class_weight assigns class weighting 
		- set parameter settings 
			line 6, num_par sets number of parameters
			line 7, par_start_col sets parameter start column from csv (0-indexed)
		- set features to iterate through for threshold analysis
			lines 12 and 13 can be edited to indicate which features the threshold analysis will iterate through
		- optional
			- filter buchwald ligands (or other variations)
				- change lines 31-32 X_use=X_all and y_use=y_all to X_use=X_nobw and y_nobw
				- toggle comment on line 76 to plot buchwald ligands in gray
			- edit plot labels
				- line 71 = experimental output (e.g., yield, selectivity)
			- save plots 
				- toggle comment on line 89
				
## Acknowledgements 
We acknowledge _____ for funding. xxxx

## Citation
This code is released under the MIT license. Commercial use, Modification, Distribution and Private use are all permitted. 
The use of this workflow can be acknowledged with the following citation: 10.26434/chemrxiv.14388557 
