# DeepAbstraction

DeepAbstraction is an open-source framework mainly used to prioritize misclassified instances among the entire unlabeled test dataset in deep learning systems. 

-------

## Steps to run the code


- [x] 1. ```pip install -r /path/to/requirements.txt```
- [x] 2. run training and test notebook. (recommended on GPU)
- [x] 3. run the processing notebook to construct monitors. 
- [x] 4. run analysis and evaluation notebook to get the results. 

-------

## Code Files Structure
* Training and test notebook: 
    * Train and test the neural network.
    * Collect high-level features during training and test.
    * identify the misclassified instances to be used later for TP evaluation.  
* Processing notebook:
    * Group high-level features into correctly classified and misclassified for each class. 
    * Construct monitors. 
    * Calcualte the entropy score and distance ratio. 
    * Collect data of the 6 types of misclassified instances while tuning tau. 
* Analysis and evaluation notebook:
    * Evaluate the effectiveness of DeepAbstraction with other baselines in prioritizing misclassified instances. 
    * Evaluate the effectiveness of DeepAbstraction and DeepGini in the near-centroid and near-boundaries regions.
    * Evaluate the removal step for the zero-scored instances. 
    * Evaluate the stability of DeepAbstraction with different values of tau with different scoring functions.


-------

## Data File Structure
* **npz folder**: contains the training and test feature vectors with labels and misclassified test instances.
* **monitors data folder**: contains both scoring functions outputs and monitors verdicts with different taus (clustering parameter).
* **tau effect folder**: contains the statistics of number of miscalssified instances with different taus.
* **Toolkit folder**: contains the functions which construct box abstraction and make the monitor verdict.

-------
## Framework Workflow[.](https://icons8.com/icons)

<img src="./images/algorithm.png"/>



-------
## Experimental Setup

<img src="./images/Datasets and Models.PNG"/>

-------
## Experimental Results

<img src="./images/table_1.PNG"/>

<img src="./images/table_2.png"/>

-------

`For any question, please feel free to contact me: hamzah.al-qadasi@univ-grenoble-alpes.fr` :email: :mailbox_with_no_mail:
