# Bank Note Authentication in R

Over the past few decades there has been a decrease in the use of currency due to recent growth in the use of electronic transactions. However, cash transactions remain very important in the global market. Hence, there is a dire need in banks and ATM machines to implement a system that classifies a note as genuine or fake.

***Is the (unseen) banknote genuine or counterfeit?***

In this project, we will build a classifier using the **KNN classification** and evaluate the performance and predictive power of a model that has been trained and tested on data collected from bank note images. A model trained on this data that is seen as a *good fit* could then be used to make certain predictions about the authenticity of a bank note.

The dataset for this project originates from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/banknote+authentication). Data was extracted from genuine and counterfeit banknote images using the Wavelet Transform tool. The dataset has 1372 instances and 5 variables.

For the purposes of this project, the following preprocessing steps have been made to the dataset:
- The columns in the dataset have no names so each one has been assigned a descriptive name using `colnames`
- Rows of data frame are shuffled since they are originally ordered.
- The features `'variance'`, `'skewness'`, `'curtosis'`, and `'entropy'` are all essential. There are no remaining **non-relevant features**. But we will compare models with different number of features.
- All features have been **multiplicatively scaled** to get all features on the same scale
- `'class'` is an integer so it is converted to a factor because it is the target attribute of the dataset which contains two values: 0 (genuine) and 1 (counterfeit)
- We don't have to balance the data since it already has a balanced ratio of 76:61 (genuine : counterfeit)
