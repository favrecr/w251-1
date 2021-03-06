# w251 - Homework 6

## BERT Toxicity Analysis

Following the instructions for HW06, I created two virtual machines, a p100 and a v100, to train a model for classifying text based on level of toxicity. Training both models in a single epoch of the data yielded total wall times of 6h 4min and 1h 51min for the p100 and v100 respectively, showing a significant performance (speed) advantage for the v100. Subsequent prediction times took 1h 1min for the p100 and 16min for the v100. Both VMs yielded similar AUC scores around 0.97, with the p100 performing slightly better.

Based on these results, and particularly the speed advantage of the v100, for Question 8 I chose to attempt training the model on two epochs of the data (A). As expected, since the model made two passes through the data, the total training time was greater at 3h 54min, more than double the single epoch on the v100 but still faster than the single epoch on the p100. However, the extra pass through the data did not improve the AUC score.

I also attempted to improve the model by adjusting the learning rate (B), however, after changing the learning rate for 2e-5 in both directions the model performance did not seem to improve.
