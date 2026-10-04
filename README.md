# Daily contacts in two age groups

This CB2330 project compares the average number of daily contacts between people aged 10–14 and those aged 70+.

We use the means and standard deviations from Table 1 in Mossong et al. (2008), *Social Contacts and Mixing Patterns Relevant to the Spread of Infectious Diseases*.

https://doi.org/10.1371/journal.pmed.0050074

## What we did

We fitted a negative binomial model for each age group and simulated contact counts using the original group sizes. We then simulated 5,000 surveys to see how much the difference between the group means varies by chance.

## Results

The published difference was 11.33 contacts per person per day. The mean simulated difference was 11.34, with a standard deviation of 0.59. The middle 95% of simulated differences fell between 10.18 and 12.48.

These results describe sampling variation under our fitted model, not all uncertainty in the original survey.

## How to run

You need Python 3, NumPy, Matplotlib and Jupyter Notebook.

1. Clone this repository and open its folder.
2. Install the packages:

   ```bash
   python -m pip install numpy matplotlib notebook
   ```

3. Start Jupyter Notebook:

   ```bash
   python -m notebook
   ```

4. Open `project.ipynb` and run all cells from top to bottom.

The notebook uses a fixed random seed and includes the published values directly, so no data download is needed.

## Files

- `project.ipynb`: model, code, figures and results.
- `data/contact_summary.csv`: published values used in the analysis.
- `data/README.md`: data source and column descriptions.
