# Machine Learning Portfolio — Prithvi Adipudi

M.S. Artificial Intelligence student (4.0 GPA, Grand Canyon University, expected May 2027) who builds models from the math up. This repo collects coursework and independent projects where I implemented backpropagation by hand in NumPy, then trained convolutional, recurrent, and ensemble models in PyTorch, TensorFlow, and scikit-learn.

prithvi.paneer@gmail.com · [LinkedIn](https://linkedin.com/in/prithvi-adipudi) · Tampa, FL

---

## Projects

| Project | Folder | Key Result | Stack |
|---|---|---|---|
| Neural Network Design & Training | `neural-network-design-and-training/` | 98.6% val. accuracy, 96.2% recall on breast cancer classification | NumPy, PyTorch |
| CIFAR-10 CNN | `cifar10-cnn/` | 80.8% accuracy, 0.805 macro F1 | TensorFlow/Keras |
| Automobile Price Prediction | `automobile-price-prediction/` | R² 0.863 → 0.882 (random forest) | scikit-learn, pandas |
| Model Evaluation | `model-evaluation/` | 90.6% vs. 88.2% test accuracy | scikit-learn, pandas |
| Ensemble Methods | `ensemble-methods/` | CV accuracy 90.2% → 94.4% | scikit-learn, pandas |

---

### 1. Neural Network Design & Training
`NumPy` `PyTorch` `scikit-learn`

- Implemented a feedforward neural network from scratch in NumPy with hand-derived backpropagation, then rebuilt it in PyTorch to benchmark optimizers — Adam reached equivalent loss ~3x faster than vanilla gradient descent.
- Built a PyTorch binary classifier on the Wisconsin Diagnostic Breast Cancer dataset, reaching 98.6% validation accuracy and 96.2% recall on malignant cases, validated at 97.0% ± 1.6% across 5-fold cross-validation.
- Trained an LSTM for next-day price forecasting on financial time-series data and demonstrated overfitting empirically: a regularized network held a 0.005 train/validation loss gap, while an oversized network's validation loss rose 7x past its turning point.

### 2. CIFAR-10 Object Recognition with Convolutional Networks
`TensorFlow/Keras` `scikit-learn`

- Designed a three-block CNN (Conv–BatchNorm–ReLU–MaxPool with staged dropout, Adam, early stopping) on 45,000 CIFAR-10 images, reaching 80.8% accuracy and 0.805 macro F1 on 5,000 stratified held-out images.
- Benchmarked it against a fully connected baseline under identical splits, preprocessing, and optimizer settings: +33.1 points of accuracy using 4.2x fewer parameters (404K vs. 1.71M), cutting errors from 2,617 to 960.
- Closed the baseline's 9-point train/validation gap to under 0.1 points with batch normalization and staged dropout, and localized residual errors to cat-dog and bird-frog confusions using per-class F1, confusion matrices, and confidence-ranked error review.

### 3. Automobile Price Prediction & Feature Selection
`scikit-learn` `pandas` `NumPy`

- Engineered three domain features (power-to-weight ratio, stroke-bore ratio, target-encoded brand prestige) for a 205-car price regression, lifting cross-validated R² from 0.772 to 0.802 for linear regression and 0.863 to 0.882 for random forest.
- Applied filter, wrapper, and embedded feature selection (mutual information, RFECV, Lasso) under a two-of-three consensus rule, reducing 62 one-hot columns to 8 (87% reduction) while improving held-out random forest R² from 0.933 to 0.941.

### 4. Model Evaluation in Machine Learning
`scikit-learn` `pandas` `NumPy`

- Compared a Logistic Regression baseline against a Random Forest on a Boston Housing classification task, scoring both on accuracy, precision, recall, F1, AUC-ROC, and Hamming loss.
- Logistic Regression edged out Random Forest on the held-out test set (90.6% vs. 88.2% accuracy, 0.962 vs. 0.959 AUC-ROC), while 5-fold stratified cross-validation narrowed that gap (86.9% vs. 87.3% mean CV accuracy) — a concrete illustration of how a single train/test split can over- or understate a model's true performance.
- Extended the analysis with repeated stratified k-fold validation to sanity-check the stability of both models' scores.

### 5. Ensemble Methods
`scikit-learn` `pandas` `NumPy`

- Compared a single decision tree against a bagging ensemble of 200 identical trees on the 3-class Wine dataset, holding the base learner and data constant so any accuracy gap is attributable to the ensembling itself.
- Bagging raised 5-fold CV accuracy from 90.2% to 94.4% and nearly halved its standard deviation (0.059 → 0.041), while held-out test accuracy rose from 94.4% to a perfect 100%.

---

## Skills

**Machine Learning:** PyTorch, TensorFlow/Keras, scikit-learn, NumPy, pandas, Matplotlib · CNNs, MLPs, LSTMs, batch normalization, dropout, ensembles, feature engineering, cross-validation
**Languages:** Python, Java 17, SQL, TypeScript, JavaScript, C#
**Engineering & Data:** Spring Boot, REST APIs, JDBC, Angular, Maven, Oracle Database, Git, Jira, Tableau

## About Me

M.S. Artificial Intelligence candidate (4.0 GPA, expected May 2027) seeking machine learning and applied AI roles. Alongside these ML projects, I deliver production Java 17 / Spring Boot services on a 5-person Agile team at DTCC.

[LinkedIn](https://linkedin.com/in/prithvi-adipudi) · [GitHub](https://github.com/prithviadip)
