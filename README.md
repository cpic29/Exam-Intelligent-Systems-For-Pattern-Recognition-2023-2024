# ISPR

_Collection of midterm projects for the Intelligent Systems for Pattern Recognition course._

Dataset: https://archive.ics.uci.edu/dataset/360/air+quality


## Midterm 1:
Consider the dataset. This is a multivariate timeseries,  where features represent measurement from different air quality sensors (every hour for a year). There are missing values marked with value -200. For this reasons I suggest to discard feature NMHC(GT) as it has far too many missing values. For the other features (sensors), handle the missing value by imputation: e.g. use the average value between the preceeding and the following observation or, if many missing value are in a row, copy the measurament from the same sensor, same time, but the day before (or after, up to you).

Analyse the correlation of the sensor measuramentes by computing the cross-correlation between the timeseries corresponding to the different sensors. Are there sensors wich are more correlated? Are there sensors which are less correlated? Report you considerations on the analysis.



## Midterm 2:
Fit an Hidden Markov Model to the data in the dataset: it is sufficient to focus on a single column of the dataset of your choice (i.e. choose one of the sensors available and focus on analysis that single sensor). Experiment with training  HMMs with two different choices of the emission distribution and confront the results.  Experiment also with HMMs with a varying number of hidden states (e.g. at least 2, 3 and 4) and identify what is the best choice according to your own reasoning. 

Once you have identified the best HMM configuration (emissions and number of states), choose a reasonably sized subsequence (e.g. last 25% of the timeseries) and compute the optimal assignement using two methods: i) Viterbi (true optimal) and ii) best state according to the hidden state posterior (very local decision). Then plot the timeseries data highlighting (e.g. with different colours) the hidden state assigned to each timepoint by the Viterbi algorithm and the posterior method.  Discuss the results.

## Midterm 3:
Train a neural network for sequences of your choice (LSTM, GRU, Convolutional, Clockwork RNN, ...) to predict the Benzene (C6H6 column) based on the sensor measurements timeseries (PT08.* columns) being fed in input to the recurrent model. Evaluate the predictive accuracy of the network on the task (using appropriately training/validation splits).  Confront the perfomance of this model, with another recurrent neural network trained to predict benzene one-step-ahead, i.e. given the current benzene measuement, predict its next value.
Show and compare performance of both settings.


## Midterm 4: 
Read and summarize the main findings of a single paper. Chosen paper: _Aditya Ramesh et al. “Hierarchical Text-Conditional Image Generation with CLIP Latents." arxiv Preprint arxiv:2204.06125 (2022)_
