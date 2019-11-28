# Dynamic Weighted Majority by Alejandro González

This repository contains the necessary files to run the Dynamic Weighted Majority algorithm (DWM). The DWM algorithm copes with the problem of concept drift in the domain of Data Streaming. Concept drift is characterized by a changing of the labels of the data throughout the time. This phenomena makes very difficult to traditional machine learning algorithms to learn from this evolving data.

In a glimps Dynamic Weight Majority implemets an ensemble classifier of online learners, such as Naive Bayes. The online learners predict the new upcoming sample from the stream and reduce their weight depending in the correctness of the rpediction. If the overal prediction is incorrect a new learner is added to the ensemble. On the pther hand, if the weight of one learner is lower than a threshold, the learner is dropped from the ensemble.

More information in the original paper: https://ieeexplore.ieee.org/document/1250911

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

The project is very simple to be deployed. It consist of a single notebook. The notebook can be run in a python environment and all the cells executed. All the functions and sketches of code are commented and the Input and Output are stated. The structure of the code is as follows.

The code is mainly divided in three sections:

1. **Functions**: This section includes all the functions necessary to execute the complete algorithm. This functions are:
  1. *norm_weights*
  1.2 *remove_experts*
  3. *avg_acc*
  4. *replace_experts*
  5. *plot_performance*
  
2. **Stagger**: In this section first a *Stagger concept* dataset is built. Later on DWM is implemented by using the previous functions using as data the Stagger concept dataset. The algorithm is run one time and ten tiumes to compute the evolution of the average of accuracy and number of learners.

3. **SEA**: In this section a dataset of *SEA concepts* is built and later on the DWM is trained with that dataset. Here several variants are performed, such as limiting the maximum number of learners to 5 or updating the learners every ***p*** time steps.


### Prerequisites

In order to run the notebook it is necessary to have python or a python environment installed with the following libraries:

* sklearn
* pandas
* numpy
* matplotlib
* tqdm
* warnings

## Running the tests

For each of the Datasets *STAGGER concepts* and *SEA concepts* a test is performed. The test can be run in a lopp of k times in order to compute accuracy averages

## Authors

* **Alejandro González**


## Acknowledgments

This project has been developed for the master course Data Streaming.

