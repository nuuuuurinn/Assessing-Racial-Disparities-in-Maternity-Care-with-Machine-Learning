## Setup Instructions
1. Download **final_code.py** to a folder on your computer.
2. Download **DATASET.csv** in the same folder as final_code.py.

## Run the Code
1. Open your terminal or command prompt, navigate to the folder containing your files, and run the script:
```
python final_code.py
```
_Note: Depending on your computer's speed and the size of the dataset, it may take a few minutes to train the models and output the final results._


2. When the script finishes running, it will automatically create a new folder called Finalproject/outputs/ in your current directory, containing:
  A. train_data.csv – The 60% of data used to train the model.

  B. validation_data.csv – The 20% of data used to compare the models.

  C. test_data.csv – The final 20% of data used to evaluate the best model.

  D. model_metrics.txt – A text file containing a permanent record of your models' performance, including F1 scores, Recall, Precision, AUPRC, the Confusion Matrix, and the full Classification Report.

## Understanding the Results
When you view the final metrics, you will likely notice a high recall but a very low precision.
This is entirely expected and by design.
Because we are predicting a rare, life-threatening medical event, the model is configured to act like a highly sensitive smoke detector. It trades precision for recall, meaning it throws many "false alarms" (low precision) in order to successfully catch as many actual SMM cases as possible (high recall).
