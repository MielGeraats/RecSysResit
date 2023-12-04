# Recommender Systems Resit Project - Miel Geraats, i6260213

This project uses pre-existing movies and ratings datasets. The Main.py file uses a Hold-Out Validation
Strategy to train a UserUser Collaborative Filtering model on the previously mentioned datasets.
The model then makes predictions for the users on the test set of the Hold-out split.
Random groups of size 4 are then generated, for whom recommendations are made using 2 different
aggregation strategies: Additive and Least Misery. When all recommendations are done, both strategies are
evaluated using nDCG evaluation. An average value is calculated for both strategies, after which a conclusion
is made for which strategy generated the best recommenations based on the nDCG value

An important note is that both the group generation and the hold-out validation is done using random states
on every repeat run of the code, meaning different results will appear every time the code is ran. 
In the provided excel file, the results from 10 runs are compared. Looking at these results, it is clear
the Additive aggregation strategy has a higher nDCG score on average, though for some runs it is very close
and the Least Misery strategy even scored higher on 1 run, meaning their performance is comparable at least.

## Prerequisites

Make sure you have the following installed:

- Python 3.11
- Required Python packages:
  - pandas
  - numpy
  - scikit-learn
  - lenskit
