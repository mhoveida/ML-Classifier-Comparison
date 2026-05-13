This project involves two main parts: a comparative study of various machine learning **classifiers** on a non-linearly separable dataset and an exploration of the **Curse of Dimensionality**.

### Part I: Classification Analysis

Five different classifiers were tested on a dataset with a "checkerboard-like" structure, meaning the classes are not linearly separable and require complex decision boundaries.

| Classifier | Training Score | Testing Score | Key Observations |
| --- | --- | --- | --- |
| **Decision Tree** | 0.9733 

 | <br>**0.995** 

 | <br>**Best performer.** Learned training patterns perfectly and generalized excellently to unseen data.

 |
| **Random Forest** | 0.944 

 | 0.945 

 | Second best; combines multiple trees to help generalize better, though slightly lower accuracy than a single tree here.

 |
| **KNN** | 0.93 

 | 0.925 

 | Third place; effectively captured the shape of the data distribution with a flexible boundary.

 |
| **AdaBoost** | 0.6133 

 | 0.63 

 | Performed poorly; the simple rectangular boundaries of the weak learners failed to capture complex patterns.

 |
| **Logistic Regression** | 0.6067 

 | 0.565 

 | <br>**Worst performer.** Its linear nature limits its ability to handle complex, non-linear patterns.

 |

### Part II: The Curse of Dimensionality

The "Curse of Dimensionality" refers to the phenomenon where, in high-dimensional spaces, data points become nearly equidistant from one another. This makes distance-based methods like **KNN** difficult to use effectively.

* 
**Distance Ratio ($D_{max}/D_{min}$)**: The experiment tracked how the ratio of the farthest distance to the nearest distance changes from $d=1$ to $d=100$.


* 
**Trend**: In low dimensions ($d < 20$), the $\log(D_{max}/D_{min})$ decreases rapidly.


* 
**Stabilization**: After $d > 20$, the ratio levels off for all sample sizes, showing that distances become nearly uniform.


* 
**Sample Size Impact**: Larger datasets ($N=1000, 5000$) produced smoother lines with less noise compared to smaller datasets.



### Part III: Curse or Blessing?

While high dimensionality presents challenges like processing speed and noise from useless features, it also offers a **"Blessing of Dimensionality"**.

* 
**Separability**: Higher dimensions can make it easier to sort different types of data, such as distinguishing tissue types in medical imaging.


* 
**Pattern Discovery**: More features can reveal hidden relationships, leading to better predictions in fields like finance.


* 
**Generalization**: Large models (e.g., in NLP) can actually reduce overfitting in high dimensions by being forced to generalize across many features.



To manage these spaces, researchers utilize techniques such as **dimensionality reduction**, **feature selection**, and **regularization**.