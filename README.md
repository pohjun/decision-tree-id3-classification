# Student Performance Classification with Decision Trees

This project explores binary classification of student performance using decision tree models.

It includes both a scikit-learn Decision Tree classifier and a custom ID3-style implementation. The project compares their behaviour, evaluates classification performance, visualises the learned decision tree, and investigates how tree depth affects model generalisation.

## Project Overview

The objective of this project is to classify student outcomes into two classes:

- Pass
- Fail

The workflow includes data preprocessing, model training, evaluation, visualisation, and comparison between a custom ID3 implementation and a scikit-learn reference model.

## Methods Used

The project includes:

- Data preprocessing
- Train-test splitting
- Decision Tree classification
- Custom ID3-style classification
- Accuracy evaluation
- Precision, recall and F1-score
- Confusion matrix analysis
- Decision tree visualisation
- Tree depth experiments
- Comparison between training and test accuracy

## Technologies

- Python
- pandas
- NumPy
- scikit-learn
- matplotlib
- Google Colab

## Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrices

The results show that overall accuracy alone is not enough to evaluate the classifier, because the models performed much better at identifying Pass cases than Fail cases.




































## Scikit-learn Decision Tree Results

The scikit-learn Decision Tree produced the following confusion matrix:

| Actual / Predicted | Fail | Pass |
|---|---:|---:|
| Fail | 5 | 15 |
| Pass | 13 | 97 |

The model correctly identified most Pass cases but struggled to identify Fail cases.

This class imbalance in predictive performance can also be seen in the classification report, where precision and recall for the Fail class were considerably lower than for the Pass class.

## Custom ID3 Results

The custom ID3 implementation produced a very similar confusion matrix:

| Actual / Predicted | Fail | Pass |
|---|---:|---:|
| Fail | 5 | 15 |
| Pass | 14 | 96 |

The similar results between the custom ID3 model and the scikit-learn model provide a useful behavioural comparison.

However, the models are not expected to be identical because their handling of continuous variables and split selection may differ.



## Tree Depth Experiment

Different maximum tree depths were tested to examine the effect of model complexity on training and test performance.

The best test performance in the experiment was achieved with:

- Maximum depth = 5
- Test accuracy = 82.31%

The unrestricted tree achieved:

- Training accuracy = 96.15%
- Test accuracy = 77.69%

This indicates that increasing tree complexity improved training performance but reduced generalisation to unseen data.

The unrestricted tree therefore showed signs of overfitting.

## Decision Tree Visualisation

The trained decision tree was visualised to show how features were used to split the data and classify student outcomes.

This helped make the model easier to interpret and showed how decisions were made across different branches of the tree.

## Key Findings

The main findings from this project were:

- Decision tree depth had a noticeable effect on generalisation.
- A deeper tree did not necessarily produce better test accuracy.
- The unrestricted tree showed signs of overfitting.
- Both models performed better on Pass cases than Fail cases.
- The custom ID3 model produced results similar to the scikit-learn reference model.
- Accuracy should be interpreted together with precision, recall and the confusion matrix.





























## Project Structure

```text
decision-tree-id3-classification/
├── README.md
├── ID3_Student_Performance.ipynb
├── requirements.txt
└── images/
    ├── confusion_matrix.png
    ├── id3_confusion_matrix.png
    ├── decision_tree.png
    └── depth_comparison.png
```

## Requirements

Example Python dependencies:

pandas
numpy
scikit-learn
matplotlib

## How to Run

1. Open the notebook in Google Colab or Jupyter Notebook.
2. Install the required libraries.
3. Load the dataset.
4. Run the notebook cells in order.
5. Review the model evaluation, confusion matrices and decision tree visualisation.

## What I Learned

This project helped me develop practical experience in:

* Building classification models
* Implementing decision tree logic
* Comparing a custom algorithm with a library implementation
* Evaluating models using multiple metrics
* Identifying overfitting
* Interpreting confusion matrices
* Visualising decision trees
* Communicating machine learning results

## Author

Song
