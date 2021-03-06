# Contextual Bandits Decision Tree

This repo houses a python implementation of the decision tree designed by
Feraud, R. , Allesarido, R. , Urvoy, T. & Clerot, F.
in [*Random Forest for the Contextual Bandit Problem*](https://arxiv.org/pdf/1504.06952.pdf)

The orignal version was only designed for use with binary variables, however, 
additions have been made to allow for continuous and categorical variables.
A statistical test has also been added to each feature-value split to ensure only statistically significant results are used.

The tree consists of nodes which will choose the best feature and value to split on according to expected maximum reward when using the variable to select the best action. Action selection is then achieved at each leaf node by using Thompson Sampling, that is, modeling each possible action with a Beta distribution with a = #clicks and b=#opens.

Currently a proportion z-test is being used to test for statistical significance so only 2 actions are available in its current form, however I plan on switching to a proportion chi square test to allow for more actions.

[Algorithm Visualization](Contextual%20Bandits%20Decision%20Tree%20Visual.pdf)

![](Decision_Tree_Visual.png)


## Usage
[Walk Through of Decision Tree Usage](Contextual_Bandits_Decision_Tree_Walk_Through.ipynb)

[Simulated Data Creation](Simulated%20Data.ipynb)


## Requirements/Dependencies
* python 3
* numpy
* pandas
* statsmodels
* random


## Citation
* **Feraud, Raphael** - *Author* - [Random Forest for the Contextual Bandit Problem](https://arxiv.org/pdf/1504.06952.pdf)
* **Allesarido, Robin** - *Author* - [Random Forest for the Contextual Bandit Problem](https://arxiv.org/pdf/1504.06952.pdf)
* **Urvoy, Tanguy** - *Author* - [Random Forest for the Contextual Bandit Problem](https://arxiv.org/pdf/1504.06952.pdf)
* **Clerot, Fabrice** - *Author* - [Random Forest for the Contextual Bandit Problem](https://arxiv.org/pdf/1504.06952.pdf)

## Acknowledgments
The decision tree python code structure was heavily inspired by the following sources:

* https://lethalbrains.com/learn-ml-algorithms-by-coding-decision-trees-439ac503c9a4
* https://medium.com/@curiousily/building-a-decision-tree-from-scratch-in-python-machine-learning-from-scratch-part-ii-6e2e56265b19
* https://towardsdatascience.com/random-forests-and-decision-trees-from-scratch-in-python-3e4fa5ae4249
* https://machinelearningmastery.com/implement-decision-tree-algorithm-scratch-python/
