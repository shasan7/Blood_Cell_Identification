# Blood Cell Identification using MaxViT-nano

## Dataset Link: https://www.kaggle.com/datasets/paultimothymooney/blood-cells/

## Kaggle Notebook: https://www.kaggle.com/code/shasan7/blood-cell-identification/


The images were transformed and normalized using torch, then we fed them to the **pretrained MaxViT-nano model for fine-Tuning**.

**The best validation accuracy achieved by our model is 100%**.

Training Summary:

    Epoch [1/20]  Train Loss: 0.2338 | Train Acc: 90.59%  || Val Loss: 0.0825 | Val Acc: 96.24%
    Saved new best model with val_acc: 96.24%
    Epoch [2/20]  Train Loss: 0.0816 | Train Acc: 97.12%  || Val Loss: 0.0409 | Val Acc: 98.64%
    Saved new best model with val_acc: 98.64%
    Epoch [3/20]  Train Loss: 0.0530 | Train Acc: 98.24%  || Val Loss: 0.0096 | Val Acc: 99.64%
    Saved new best model with val_acc: 99.64%
    Epoch [4/20]  Train Loss: 0.0411 | Train Acc: 98.71%  || Val Loss: 0.0407 | Val Acc: 98.84%
    Epoch [5/20]  Train Loss: 0.0372 | Train Acc: 98.74%  || Val Loss: 0.0097 | Val Acc: 99.72%
    Saved new best model with val_acc: 99.72%
    Epoch [6/20]  Train Loss: 0.0260 | Train Acc: 99.21%  || Val Loss: 0.0083 | Val Acc: 99.76%
    Saved new best model with val_acc: 99.76%
    Epoch [7/20]  Train Loss: 0.0307 | Train Acc: 98.98%  || Val Loss: 0.0440 | Val Acc: 99.28%
    Epoch [8/20]  Train Loss: 0.0357 | Train Acc: 98.89%  || Val Loss: 0.0731 | Val Acc: 98.12%
    Epoch [9/20]  Train Loss: 0.0200 | Train Acc: 99.31%  || Val Loss: 0.0015 | Val Acc: 99.92%
    Saved new best model with val_acc: 99.92%
    Epoch [10/20]  Train Loss: 0.0251 | Train Acc: 99.22%  || Val Loss: 0.0329 | Val Acc: 99.16%
    Epoch [11/20]  Train Loss: 0.0251 | Train Acc: 99.32%  || Val Loss: 0.0127 | Val Acc: 99.72%
    Epoch [12/20]  Train Loss: 0.0179 | Train Acc: 99.51%  || Val Loss: 0.0307 | Val Acc: 98.96%
    Epoch [13/20]  Train Loss: 0.0190 | Train Acc: 99.48%  || Val Loss: 0.0034 | Val Acc: 99.92%
    Epoch [14/20]  Train Loss: 0.0208 | Train Acc: 99.49%  || Val Loss: 0.0541 | Val Acc: 98.44%
    Epoch [15/20]  Train Loss: 0.0217 | Train Acc: 99.38%  || Val Loss: 0.0034 | Val Acc: 100.00%
    Saved new best model with val_acc: 100.00%
    Epoch [16/20]  Train Loss: 0.0066 | Train Acc: 99.79%  || Val Loss: 0.0012 | Val Acc: 99.92%
    Epoch [17/20]  Train Loss: 0.0202 | Train Acc: 99.35%  || Val Loss: 0.0108 | Val Acc: 99.60%
    Epoch [18/20]  Train Loss: 0.0202 | Train Acc: 99.39%  || Val Loss: 0.0007 | Val Acc: 100.00%
    Epoch [19/20]  Train Loss: 0.0186 | Train Acc: 99.51%  || Val Loss: 0.0066 | Val Acc: 99.84%
    Epoch [20/20]  Train Loss: 0.0150 | Train Acc: 99.59%  || Val Loss: 0.0018 | Val Acc: 99.92%


Obtained Results:

                  precision    recall  f1-score   support
    
      EOSINOPHIL       1.00      1.00      1.00       627
      LYMPHOCYTE       1.00      1.00      1.00       622
        MONOCYTE       1.00      1.00      1.00       620
      NEUTROPHIL       1.00      1.00      1.00       634
    
        accuracy                           1.00      2503
       macro avg       1.00      1.00      1.00      2503
    weighted avg       1.00      1.00      1.00      2503


Confusion Matrix:

    [[627   0   0   0]
     [  0 622   0   0]
     [  0   0 620   0]
     [  0   0   0 634]]


![Confusion Matrix: ](Conf_Mat.png)

![Accuracy Curve: ](Acc.png)

![Loss_Curve): ](Loss.png)

