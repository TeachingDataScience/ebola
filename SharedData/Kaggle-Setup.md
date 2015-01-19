
Once a basic Kaggle competition is setup, the competition can be transferred to Kaggle's main platform, reviewed by Kaggle professionals, and broadcast.

* [Competition Wizard Link](https://inclass.kaggle.com/join/k2k4-ugugzx-pvx3) (to edit competition)


## Blockers

### Publically Available Data?

Publically available data answer keys might make the competition moot.  However, other groups have used potentially publically available data in their competitions -- like this bicycle demand prediction:

http://www.kaggle.com/c/bike-sharing-demand/data

The competition is to predict demand, and the answer format (excerpt) is:

	datetime,count
	2011-01-20 13:00:00,0
	2011-01-20 14:00:00,0
	2011-01-20 15:00:00,0
	2011-01-20 16:00:00,0
	2011-01-20 17:00:00,0
	2011-01-20 18:00:00,0
	2011-01-20 19:00:00,0
	2011-01-20 20:00:00,0
	2011-01-20 21:00:00,0
	2011-01-20 22:00:00,0
	2011-01-20 23:00:00,0
	2011-01-21 00:00:00,0
	2011-01-21 01:00:00,0
	2011-01-21 02:00:00,0
	2011-01-21 03:00:00,0
	2011-01-21 04:00:00,0
	2011-01-21 05:00:00,0
	2011-01-21 06:00:00,0

However, they simply used the following note to ensure 'honesty':

* Due to the public nature of the data, this competition does not count towards Kaggle ranking points.
* We ask that you respect the spirit of the competition and do not cheat. You should not submit entries based on test-set answers or train your model on the test set. Hand labeling is also forbidden.
* Your model should only use information which was available prior to the time for which it is forecasting.

Perhaps this is the way to go(?)

## Basic Model

The most simple model would be appropriate to start with.

**Possible Targets**

* Projections of Future Cases
  *  As used by [mobs lab](http://www.mobs-lab.org/ebola.html)
* Case Fatality Rate
   * Grew from 53% to 71%
* Estimating the reproduction number
    (currently between 1.5 and 2.5)
    
* Which characteristics of tweets predict an accelerated output?
   * EbolaTracking.org uses mentions on a map.

**Factors / Available Data**

*Note: Generally the [HDX Site](https://data.hdx.rwlabs.org/ebola) is the most complete and convenient data source*

* Transmission Methods
    * Within families
    * In hospitals 
    * at funerals
 
 * Geographic Data
     * assembled by [geonode ](http://www.ebolageonode.org/)
	* Boundaries 22
	* Health 10
	* Inland Waters 8
	* Location 3
	* Society 4
	* Transportation 11
	* Utilities Communication

* Resource Flows
   * By [donor and country](http://www.worldbank.org/en/topic/ebola/brief/global-ebola-response-resource-tracking)
   * [Financial Tracking Service Page](http://fts.unocha.org/pageloader.aspx?page=emerg-emergencyDetails&emergID=16506)
   * ![](http://note.io/1AUDrP7)
   
* Cases by districts
* Availability of Safe Burial TEams
   
   
    




**Training and Test Set**






**Scoring Metrics**

The analagous "Bike Sharing" competition used RMSLE.

#### RMSLE EVALUATION

Evaluating via the Root Mean Squared Logarithmic Error (RMSLE). The RMSLE is calculated as

![](http://note.io/1BVWGJX)

Where:

* n is the number of days in the test set
* pi is your predicted mortality count
* ai is the actual mortality count
* log(x) is the natural logarithm


These are the possible metrics:

* AUC (Area Under Receiver Operating Characteristic Curve) [binary-classification]
* Gini (Gini Index) [binary-classification]
* LogLoss (Log Loss) [binary-classification]
* MCAUC (Mean Columnwise Area Under Receiver Operating Characteristic Curve) [binary-classification]
* MeanUtility (MeanUtility) [binary-classification]
* CategorizationAccuracy (Categorization Accuracy) [multiclass-classification]
* MulticlassLoss (Multiclass Loss) [multiclass-classification]
* CorrelationCoefficient (CorrelationCoefficient) [regression]
* MAE (Mean Absolute Error) [regression]
* MCRMSE (Mean Columnwise Root Mean Squared Error) [regression]
* NormalizedGini (Normalized Gini Index) [regression]
* NWMAE (Normalized Weighted Mean Absolute Error) [regression]
* RMSE (Root Mean Squared Error) [regression]
* RMSLE (Root Mean Squared Logarithmic Error) [regression]
* SpearmanR (SpearmanR) [regression]
* MAP@{K} () [other]
* GestureNormalizedLevenshteinMean (Gesture Normalized Levenshtein Mean) [other]
* IntegerLevenshteinMean (Integer Levenshtein Mean) [other]
* LevenshteinMean (Levenshtein Mean) [other]
* MCE (Mean Consequential Error) [other]
* MeanFScore (Mean F-Score) [other]


### Resources

* [Kaggle In-Class Instructions](https://www.kaggle.com/wiki/KaggleInClass)
