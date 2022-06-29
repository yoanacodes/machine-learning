## Regularization parameter - SVC()

Task: *Introduce changes to show the effect of multiple alterations on a margin size parameter (C) for the Support Vector Machines classifier (SVC) in scikit-learn.*

Due to the long time required to run the SVC model, other similar models were included in the notebook: Linear SVR and Linear SVC.

#### Iterations:
* Linear SVR
	* default parameters
	* max_iter=1000000 
	* max_iter=1000000000
	* C=0.0001
* Linear SVC
	* default parameters
	* C=100
	* C=1000000
	* C=0.001
	* C=1e-15
	* C=1e-323
* SVC
	* C=1e-15, kernel='linear'
	* C=1e-323, kernel='linear'

All iterations of the Linear SVR resulted in no predictions, and the model was not included in the ROC plots.

<br/>

Before introducing any changes, Linear SVC performed as follows:
###### Linear SVC
![](graphs/linear_SVC_default.png)

SVC with default parameters did not execute, so only iterations that executed were visualized.

<br/>

Graphs representing the performance:
###### Linear SVC C=100
![](graphs/linear_SVC_100.png)
###### Linear SVC C=1000000
![](graphs/linear_SVC_1m.png)
###### Linear SVC C=0.001
![](graphs/linear_SVC_001.png)
###### Linear SVC C=1e-15
![](graphs/linear_SVC_1e-15.png)
###### Linear SVC C=1e-323
![](graphs/linear_SVC_1e-323.png)
###### SVC C=1e-15
![](graphs/SVC_1e-15.png)
###### SVC C=1e-323
![](graphs/SVC_1e-323.png)

<br/>

For easier comparison, here I show the ROC plots and Accuracy comparison between all iterations:

###### ROC train set
![](graphs/ROC_train.png)
###### ROC test set
![](graphs/ROC_test.png)
###### Accuracy comparison
![](graphs/accuracy_bar.png)
###### Precision comparison
![](graphs/precision_bar.png)

