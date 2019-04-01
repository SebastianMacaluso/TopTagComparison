# Top Tagging Comparison Analysis

### **Kyle Cranmer, Gregor Kasieczka, Sebastian Macaluso and David Shih**


[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)


-------------------------------------------------------------------------
## Introduction

This folder contains part of the code used for the comparison analysis published in  ["The Machine Learning Landscape of Top Taggers"](https://arxiv.org/abs/1902.09914). Abstract of the paper:

*"Based on the established task of identifying boosted, hadronically decaying top quarks, we compare a wide range of modern machine learning approaches. We find that they are extremely powerful and great fun."*

The files with the output probabilities of each tagger were provided by the individual groups, as described in the [paper](https://arxiv.org/abs/1902.09914). These files are not part of this repository.



-------------------------------------------------------------------------
## Dependencies

Make sure the following tools are installed and running:

- Packages included in [Anaconda](https://www.anaconda.com/) (Jupyter Notebook, Numpy, Scipy, scikit-learn, Pandas)

-------------------------------------------------------------------------
## Top Tagging Reference Dataset

A description and link to the *Top Tagging Reference Dataset* (provided by Gregor Kasieczka, Michael Russel and Tilman Plehn) can be found [here](https://docs.google.com/document/d/1Hcuc6LBxZNX16zjEGeq16DAzspkDC4nDTyjMp1bWHRo/edit)
with the link to download it [here](https://desycloud.desy.de/index.php/s/llbX3zpLhazgPJ6). This dataset contains 1.2M training events, 400k validation events, 400k test events with equal numbers of top quark and qcd jets. Only 4-momentum vectors of the jet constituents.

-------------------------------------------------------------------------
## Contents 

-[`jet_study_allTaggers.ipynb`](jet_study_allTaggers.ipynb): Jupyter Notebook that performs the comparison analysis. 
<!--If viewing on GitHub, this looks better with nbviewer: [click here](https://hub.mybinder.org/user/sebastianmacalu-pjetscomparison-fpa2oyx1/notebooks/jet_study_allTaggers.ipynb)-->

-[`jets_kinematics`](jets_kinematics): Kinematic variables (*E, eta, phi, pz*) values obtained from reclustering the jet constituents of the test set of the [*Top Tagging Reference Dataset*](https://docs.google.com/document/d/1Hcuc6LBxZNX16zjEGeq16DAzspkDC4nDTyjMp1bWHRo/edit).

-[`ROC_allTaggers.pdf`](ROC_allTaggers.pdf): ROC curve of each algorithm for the model that gives the median AUC out of all the 9 models.

-[`plot_bar_flatten.pdf`](plot_bar_flatten.pdf): Bar plot showing the background rejection at 30% tag efficiency for the model with the median AUC for each algorithm. This plot shows values for the original dataset and after reweighting the output probabilities so as to flatten the *pT, eta, pz and E* distributions.

-[`labels.pkl`](labels.pkl): Labels of the test set with the truth values for each jet.

-------------------------------------------------------------------------
## References

Please cite this code as

```
@misc{TopJetsComparison,
author       = "K. Cranmer, G. Kasieczka, S. Macaluso and D. Shih",
title        = "{Subset of the code used for the Top Tagging Comparison Analysis}",
note         = "{DOI: }",
year         = {2019},
url          = {https://github.com/SebastianMacaluso/TopTagComparison}
}
```
