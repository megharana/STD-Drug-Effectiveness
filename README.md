## Prequisites:
* Python 3

## Instruction to run on Jupyter notebook:

* Clone the repository 
* Download the dataset from drive : [Dataset](https://drive.google.com/uc?export=download&id=1ShQXEn1xFh5Ze42vn3InTQ27SifzbiYW)
* Unzip and place inside STDDrugEffectiveness folder.
* Open Terminal and navigate till the STDDrugEffectiveness folder. 
* Create virtual Directory inside STDDrugEffectiveness folder  using following link : [Link](https://docs.python.org/3/tutorial/venv.html)
* Run following commands based on OS platform to activate the virtual directory:
    NOTE : change <vir_dir_name> with the virtual directory name given in above step.
    IOS/Linux : ```source <vir_dir_name>/bin/activate```
    Windows :```<vir_dir_name>\Scripts\activate.bat```
* Run the following command, in order to install all libraries needed to run jupyter notebook :
    ```pip install -r requirements.txt ```
* Run the following command to launch jupyter notebook : ```jupyter notebook```
* Jupyter Notebook will be launched on localhost:8888 in default browser.
 


## Approach followed:

* __Data Preprocessing__ - Cleaned pateient's review by removing stop words. Predicting sentiment of review. Scaling *effectiveness_rating*, *number_of_times_prescribed*, *Predict_Sentiment* to better results.    

* __ANN with activation function , loss function, optimizer__ - Constructed model with four  sequential layers with relu as activation function and two additional layers with drop out technique to reduce overfitting. InverseTimeDecay function is used to rgradually reduce the learning rate during training. Here metric selected is *mae* *mse* and optimizer selected is Adam and loss function as *mse*. 


* __Cross validation__ - With a small sample size like our current situation, it’s especially important to perform cross validation to get a better estimate on accuracy. Early stopping is used,that allows you to specify an arbitrary large number of training epochs and stop training once the model performance stops improving on a hold out validation dataset.

* __Predicting Test data__ - After predicting across test data, we get array of base_score of drugs.

