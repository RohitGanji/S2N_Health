
# S2N Health Data Scientist - Round 2 Assessment Project

## Project Overview

This project focuses on analyzing Medicare Physician and Other Practitioners data to identify physicians with similar practice patterns to a given target physician. By employing data cleaning, exploration, dimensionality reduction (via PCA), and nearest neighbor algorithms, we aim to highlight patterns and similarities among physicians' practices.

## Dataset

The dataset used in this project is derived from Medicare's publicly available data on Physician and Other Practitioners. It includes various metrics such as the National Provider Identifier (NPI), HCPCS codes (Healthcare Common Procedure Coding System), and total services provided.

## Prerequisites

To run the analysis, ensure you have the following installed:

- Python 3.x
- Pandas
- NumPy
- Scikit-learn

## Setup and Data Loading

Start by importing necessary libraries:

```python
import pandas as pd
import numpy as np
from sklearn.decomposition import PCA
from sklearn.metrics.pairwise import cosine_similarity
```

Load the dataset:

```python
dataset = pd.read_csv('<path_to_dataset>/Medicare_Physician_Other_Practitioners.csv')
```

## Data Exploration and Cleaning

Initial data exploration is conducted to understand the dataset's structure, followed by data cleaning to handle null values and outliers. This includes examining value counts and distributions of various columns.

## Feature Selection and Data Sampling

The analysis focuses on a target physician, identified by their NPI. We extract unique procedures performed by this physician and sample the dataset to include only those relevant entries.

## Dimensionality Reduction with PCA

To manage the high dimensionality of the data, PCA is applied to the feature set, reducing the number of dimensions while preserving variance.

## Nearest Neighbors Computation

Cosine similarity is computed between the target physician and all other physicians in the dataset to identify those with the closest practice patterns.

## Function Definition

A function `find_nearest_neighbors` is defined to encapsulate the process of finding nearest neighbors with options for using PCA and specifying the number of components.

## Usage

The notebook includes examples of using `find_nearest_neighbors` with different parameters to demonstrate its functionality.

## Findings and Conclusion

The analysis successfully identifies physicians with similar practice patterns to the given target physician. The use of PCA for dimensionality reduction and cosine similarity for nearest neighbors computation proves effective for this purpose.

## Future Work

Further analysis could involve more sophisticated algorithms for similarity computation or exploring other aspects of the data, such as geographical or temporal patterns.

---

For any questions or suggestions regarding this project, please open an issue or submit a pull request.
