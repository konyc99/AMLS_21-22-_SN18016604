![N|Solid](https://targetcareers.co.uk/sites/targetcareers.co.uk/files/public/styles/logo_320x213/public/ucl%20logo_sml_blk.jpg?itok=uBdAgP8Z)
# AMLS Assignment
## APPLIED MACHINE LEARNING SYSTEM ELEC0134 21/22

## Task introduction
This repository covers a classification task of MRI scans of human brains containing tumors. I proposes 2 ways of approaching the task – binary classification to detect the existence of any tumor and more precise detection of 3 specific types of tumors.
Two deep learning and one non-deep learning models are proposed and compared based on accuracy, memory efficiency and workload needed to preprocess the data and train the models to achieve the results.

Data was obtained from:
>Sartaj Bhuvaji, Ankita Kadam, Prajakta Bhumkar, Sameer Dedge, and Swati Kanchan, “Brain Tumor
Classification (MRI).” Kaggle, 2020, doi: 10.34740/KAGGLE/DSV/1183165

## REPO structure
This repository contains dataset, results and application of 3 machine learning models:

- Jupyter Notebook files - one per model:
  - SVM(support vecotr machine)
  - CNN (Convolutional Neural Network) binary classification type
  - CNN (Convolutional Neural Network)  categorical classification type
- Dataset - contains the images the algorithm has been trained and tested on
- __his.csv - files contain training callbacks for the CNN algoirthm to plot the training curves without rerunning the model
- plot_learning_curve.py - SVM learning curves plot function, obtained from:
-- >https://scikit-learn.org/stable/auto_examples/model_selection/plot_learning_curve.html
    

## Instructions
Each file starts with a cell of necessary libraries and additions for the code to work - make sure that does not throw any errors and install any missing packages before proceeding.Recomended to use the built in PIP:
```sh
pip install "package name"
```
Most notable requirements are:

| Library | Version |
| ------ | ------ |
|keras  |2.6.0|
| matplotlib|3.3.4|
|pandas | 1.2.4|
|pillow|8.2.0 |
|scikit-image|0.18.1 |
|scikit-learn| 0.24.1|

Make sure that files are arranged and named the same way as in the repository - if u make any changes you will have to alter the label and image paths for all algorithms as they are not universal, for exmaple:
```sh
df=pd.read_csv('dataset/image/label_binary.csv',dtype=str)
df_test=pd.read_csv('dataset/test/label_binary.csv',dtype=str)
```

Make sure that csv files stay saved as csv and are not altered - if the format is changed the algorithm will NOT work as intended.

## Addtional Features and Extras
- Trained model weights can be provided on request as they weight 0.5 and 1GB each therefore could not be included in this repository.

- Test2 is a small test set created out of the initial data for initial unseen data testing and predictions - could be removed or integrated back into the base dataset since 200 test images were given
