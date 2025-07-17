
# RandomForest Classifier from Scratch

This project contains a simple, educational implementation of the Random Forest algorithm for supervised classification tasks. It’s written in pure Python and NumPy, with a modular design so you can easily understand, extend, or integrate it with other projects.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Class and Method Documentation](#class-and-method-documentation)
- [Example](#example)
- [License](#license)
- [Contact](#contact)

---

## Overview

Random Forest is an ensemble learning method that operates by constructing a multitude of decision trees during training and outputs the class that is the mode of the classes (majority vote) of the individual trees. This repository includes:

- `RandomForest` class
- `DecisionTree` class (should be provided separately or adapted as per your needs)

---

## Features

- Build a customizable number of trees (`n_trees`)
- Supports limiting tree depth and minimum samples for split
- Bootstrapped (bagging) sampling
- Majority voting for predictions
- Fully documented and beginner-friendly

---

## Requirements

- Python 3.7 or higher
- NumPy

Install requirements with:
```bash
pip install numpy
```

---

## Installation

1. **Clone the repository or copy the source code.**
2. Make sure `DecisionTree.py` is present in the same directory (implement your own or use an existing simple version).
3. Import the `RandomForest` class in your project.

---

## Usage

```python
from RandomForest import RandomForest
import numpy as np

# Example data (X: features, y: labels)
X = np.array([[1, 2], [3, 4], [5, 6], [7, 8]])
y = np.array([0, 1, 0, 1])

# Initialize the RandomForest
clf = RandomForest(n_trees=5, max_depth=3)

# Train the model
clf.fit(X, y)

# Predict labels for new samples
predictions = clf.predict(X)
print("Predictions:", predictions)
```

**Note:** You need to have a compatible `DecisionTree` class in `DecisionTree.py`.

---

## Class and Method Documentation

### `RandomForest` Class

- `__init__(n_trees=10, max_depth=10, min_samples_split=2, n_feature=None)`: Initializes the random forest.
- `fit(X, y)`: Trains the random forest using bootstrapped datasets.
- `predict(X)`: Predicts class labels for the input data.

Each method and class is fully documented within the source code for easy understanding.

---

## Example

See the [Usage](#usage) section above for a minimal working example.

---

## License

This project is licensed for educational and personal use. For commercial or research use, please check compatibility with your requirements.

---

## Contact

For any questions or improvements, open an issue or reach out!

---
