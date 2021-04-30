# Distilling a Neural Network into a Soft Decision Tree 

This repository presents a notebook containing the necessary code in our attempt to reproduce Google Brain's Team paper Distilling a Neural Network into a Soft Decision Tree (https://arxiv.org/pdf/1711.09784.pdf). The work was done by students of the class INF8225, in Polytechnique Montréal. To run the entire notebook, **you currently need a GPU** or you'll need to adapt few lines of code.

# Architecture of the Convolutional Network 

<div id="tab:accents">

| **Layer Type** | **Units** | **Kernel Size** | **Stride** |
|:---------------|:----------|:----------------|:-----------|
| Conv.2D        | 32        | 3               | 1          |
| Conv.2D        | 64        | 3               | 1          |
| MaxPool.2D     | \-        | 2               | 1          |
| Dropout(0.25)  | \-        | \-              | \-         |
| Dense          | 128       | \-              | \-         |
| Dropout(0.25)  | \-        | \-              | \-         |
| Dense          | 10        | \-              | \-         |
| Softmax        | 10        | \-              | \-         |


</div>

# Main Results

<div id="tab:accents">

| **Model** | **Labels**     | **Acc. Val** | **Acc. Test** |
|:----------|:---------------|:-------------|:--------------|
| Conv. Net | Hard (one hot) | 99.29        | 99.28         |
| SDT       | Hard (one hot) | 90.09        | 90.75         |
| SDT       | Soft           | 90.85        | 92.09         |

</div>

For further analysis and implementation details, please refer to the pdf report joined to this repository.
