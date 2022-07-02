# Early-Parkinson-Disease-Detection-Using-Audio-Signal-Processing
Early Parkinson Disease Detection Using Audio Signal Processing with the help of Machine Learning Algorithms such as Random Forest Classifier,  Xgb Classifier, K-nn, Naive-Bayes, Decisionn Tree Classifier

# Parkinson Disease Detection Using Machine Learning
[![Open Word-Level In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1WdjG9TGtX2VeP3H1B5j9XBAOBoCvKXnL#scrollTo=012faf34)

I have used the data from UC Irvine's amazing dataset repository, specifically the [Parkinsons ML database](https://archive.ics.uci.edu/ml/machine-learning-databases/parkinsons/).

There are two datasets within this. The first is in the root folder (`parkinsons.data` which is included here too) and can be used to detect Parkinsons. 

## Approach

The Oxford Parkinson Detection Data was divided into ratio of 70:30 for training and testing of models.
Random Forest Classification Model has been fed with various hyperparameters such as maximum depth
with range [ 1, 2, 3, 4, 5 ,10 ] , n-estimators with range [ 1, 2, 3, 4, 5, 10 ], maximum features with range [
1, 2, 3, 4, 5, 10 ], minimum samples leaf with range [ 1, 2, 3, 4 ] out of which the best hyperparameter were
found using Grid Search CV [17], which were 5 for maximum depth, 10 for maximum features, 2 for
minimum samples leaf, 10 for n estimators which were used in the rest of the five models proposed to get
the high accuracy and F1-score.

Proposed Models:
1. Random Forest Classification
2. Xgb Classifier
3. K-NN
4. Naive-Bayes
5. Decision Tree Classifier

Approaches are provided in the Jupyter notebook for this repo (`ParkinsonDisease.ipynb`).

You can find more info on the datasets in UCI's database. ([info for Parkinsons detection](https://archive.ics.uci.edu/ml/machine-learning-databases/parkinsons/parkinsons.names)) ([info for UDPR](https://archive.ics.uci.edu/ml/machine-learning-databases/parkinsons/telemonitoring/parkinsons_updrs.names))

## Requirements

- Python 3 (I **highly** recommend using Anaconda as this will save you a TON of time)
- XGBoost (`pip install xgboost`)
- sklearn (`pip install scikit-learn`)
- Jupyter ([instructions](http://jupyter.org/install))
- Pandas (`pip install pandas`)
- NumPy (`pip install numpy`)

## Credits

I don't own this dataset, it's provided in the link earlier.

Citations for the datasets used:

```
'Exploiting Nonlinear Recurrence and Fractal Scaling Properties for Voice Disorder Detection', 
Little MA, McSharry PE, Roberts SJ, Costello DAE, Moroz IM. 
BioMedical Engineering OnLine 2007, 6:23 (26 June 2007)
```

```
M. A. Little, P. E. McSharry, E. J. Hunter, J. Spielman, and L. O. Ramig, “Suitability of dysphonia
measurements for telemonitoring of Parkinson’s disease,” IEEE Trans. Biomed. Eng., vol. 56, no. 4, pp.
1015–1022, 2009, doi: 10.1109/TBME.2008.2005954.


A Tsanas, MA Little, PE McSharry, LO Ramig (2009)
'Accurate telemonitoring of Parkinson.s disease progression by non-invasive speech tests',
IEEE Transactions on Biomedical Engineering (to appear).
```


