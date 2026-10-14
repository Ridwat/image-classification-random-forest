# Image Classification with Random Forest

**Adetola Ridwat Odulaja** · Academic machine learning project

A classical machine learning baseline for identifying five image categories.

**Focus:** Image preprocessing · Hyperparameter tuning · Class-level evaluation

## Question

How well can a Random Forest classifier distinguish images represented as flattened pixel values?

## Approach

The notebook loads 309 images across dalmatian, dollar bill, pizza, soccer ball, and sunflower classes. Images are resized to 64 × 64 RGB, normalized, and flattened into 12,288 features. A stratified 80/20 split reserves 62 images for testing. GridSearchCV compares 36 parameter combinations using three-fold cross-validation on the training set.

## Recorded results

| Test metric | Random Forest |
|---|---:|
| Accuracy | 66.13% |
| Weighted precision | 67.19% |
| Weighted recall | 66.13% |
| Weighted F1 | 65.31% |

Class-level results vary: pizza recall is 40%, while dollar-bill recall is 100% on only 10 test examples. These differences matter more than a single aggregate score.

## Why it matters

The project demonstrates the tradeoff between a straightforward baseline and the complexity of image recognition. It also shows why evaluation should include class-level errors and sample sizes.

## Explore the work

- [Executed notebook](IMAGE_CLASSIFICATION.ipynb)
- [Submitted report](image%20classification.pdf)

## Run

Open the notebook in Google Colab, upload the required `images.zip`, and run sequentially. The archive must contain an `images/` folder with one folder per class. The dataset ZIP is not included in this repository.

Libraries include NumPy, Pillow, Matplotlib, and scikit-learn.

## Limitations

The test set is small and raw pixels do not capture spatial structure as effectively as dedicated vision models. The documented metrics are from the saved notebook run, not a new validation run. A larger dataset and comparison with learned image features would be useful extensions.

[Explore my portfolio](https://github.com/Ridwat/Ethical-AI-Analysis/blob/main/PORTFOLIO.md)
