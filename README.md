# Fake_News_SVM_Model
As part of the ECM3420 coursework, an SVM (Support Vector Machine) model has been implemented to classify fake news.
A SVM model was chosen due to its simplicity and string performance is classification tasks. 

## **Database**
The dataset used in this project, `WELFake_Dataset.csv`, can be downloaded from [this Kaggle link](https://www.kaggle.com/datasets/saurabhshahane/fake-news-classification).

### **Instructions**
1. Download the dataset from Kaggle.
2. Place the `WELFake_Dataset.csv` file in the root directory of the project.
3. Run the program as described below.

## Dependencies
Ensure you have Python 3.9 or higher installed. Install the required libraries using the following command:
```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

## Results
The Support Vector Machine (SVM) model was trained on the `WELFake_Dataset.csv` dataset. Two kernels were evaluated: Linear and RBF. Below are the results:
- **Linear Kernel**:
  - Accuracy: 94.91%
  - Precision, recall, F1-score: all 0.95
  - Training time: 24m 34.4s
  - Testing time: 4m 11.9s
  - Confusion Matrix:
  
  |                  | Predicted Positive | Predicted Negative |
  |------------------|--------------------|--------------------|
  | **Actual Positive** | 9888 | 535 |
  | **Actual Negative** | 565 | 10641 |


- **RBF Kernel**:
  - Accuracy: 95.95%
  - Precision, recall, F1-score: all 0.96
  - Training time: 216m 39.6s
  - Testing time: 7m 0.1s
  - Confusion Matrix:

  |                  | Predicted Positive | Predicted Negative |
  |------------------|--------------------|--------------------|
  | **Actual Positive** | 9965 | 387 |
  | **Actual Negative** | 488 | 10789 |

## Key Insights
- The RBF kernel demonstrated superior accuracy and reduced false positives/negatives compared to the Linear kernel.
- However, the Linear kernel is significantly faster in both training and testing, making it the preferred choice when runtime is a critical factor.
