# Visualization of Money Market Fond Accuracy with €ster

This Python notebook provides a comprehensive guide on how to visualize the accuracy of a Money Market Fond by comparing it with the €ster. The notebook uses Python 3 along with several popular libraries including pandas, matplotlib, and sklearn.

## Instructions

1. Install the required Python libraries, if you haven't done so already. You can do this by running `pip install -r requirements.txt`.

2. Download the datasets 'euster.csv' and 'fond.csv' and save them in a directory named 'data' at the same level as the notebook. The datasets should contain the following columns:

   - 'euster.csv': DATE, VALUE
   - 'fond.csv': Date, Price

3. Run the notebook from top to bottom. You can do this in Jupyter by clicking 'Kernel' -> 'Restart & Run All'.

## How it Works

- First, the necessary libraries are imported.

- Then, the datasets are loaded into pandas DataFrames. The data is cleaned, sorted by date and stored back into their respective DataFrames.

- A function, 'calculate_non_overlapping_window_return', is defined. This function calculates the annualized return for a given window of dates.

- The data is filtered to only include data after a specified start date.

- For different window sizes from 1 to 100, the annualized return is calculated. The datasets are then merged and the tracking difference is calculated. The R2 score, which measures the proportion of the variance in the dependent variable that is predictable from the independent variable, is also calculated.

- The results are then plotted on a chart using matplotlib. Two lines are plotted, one for the best R2 score and one for the best tracking difference. The €ster value is also plotted.

## Results

The output of the notebook is a plot showing the annualized returns and the €ster value over time. This plot can be used to visualize how accurately the Money Market Fond is replicating the €ster.

## Limitations

Please note that this notebook assumes that your data is well-formatted and contains no missing or erroneous values. If this is not the case, you may need to perform additional data cleaning steps not covered in this notebook.


