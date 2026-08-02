# Assignment 2 Stage 1

## Model
A small neural sentiment classifier using:
- regex tokenization
- a vocabulary built only from the training split
- `EmbeddingBag` mean pooling
- a 64-unit hidden layer with ReLU
- dropout
- a two-class output layer

## Handling the small and imbalanced dataset
- stratified 80/20 train-validation split
- inverse-frequency class weights
- dropout and AdamW weight decay
- early stopping
- `<UNK>` handling for unseen words

## Training settings
- optimizer: AdamW
- learning rate: 0.003
- batch size: 16
- maximum epochs: 30
- early-stopping patience: 5

## Public-test result
- accuracy: **0.6675**
- confusion matrix, rows=true and columns=predicted:

```text
[[119  81]
 [ 52 148]]
```

## Run
Place `train.csv` and `public_test.csv` in the repository root.

Open `stage1_notebook.ipynb` and run all cells.

## Use of AI
Generative AI was used to help organize the notebook, explain the method, and review code. The model was trained only on `train.csv`. `public_test.csv` was used only for evaluation and predictions.
