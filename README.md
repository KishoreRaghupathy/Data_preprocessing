### Data Preprocessing Pipeline

This repository contains the implementation of a data preprocessing pipeline designed to handle and clean a dataset, making it ready for machine learning modeling or data analysis tasks. The preprocessing steps include handling missing values, detecting and addressing outliers, scaling numerical features, and imputing categorical features.

#### Prerequisites

Before you can run this project, ensure that you have the following installed:
- Python 3.6 or higher
- pandas library
- numpy library
- scikit-learn library

You can install the necessary libraries using pip:

```bash
pip install pandas numpy scikit-learn
```

#### Usage

1. Clone this repository to your local machine.
2. Place your dataset in the repository folder and rename it to `data.csv` or modify the data loading line in the script to match your file's path.
3. Run the script using the following command:

```bash
python preprocessing_pipeline.py
```

#### Files

- `preprocessing_pipeline.py` - This file contains the implementation of the data preprocessing pipeline.

#### Data Preprocessing Pipeline Details

The pipeline processes the data through several stages:

1. **Identification of Feature Types**: Separates numeric and categorical features.
2. **Missing Values Handling**:
   - Fills missing values in numeric features with the mean of their respective columns.
   - Fills missing values in categorical features with the mode.
3. **Outlier Detection and Handling**:
   - Uses the Interquartile Range (IQR) method to detect and handle outliers in numeric columns. Values identified as outliers are replaced with the mean of the column.
4. **Feature Scaling**:
   - Scales numeric features using the `StandardScaler` from scikit-learn, which standardizes features by removing the mean and scaling to unit variance.

#### Example Output

After processing, the data is transformed with numeric features normalized and outliers addressed, making it suitable for further analysis or model training.

```plaintext
Preprocessed Data:
   NumericFeature1  NumericFeature2 CategoricalFeature
0    -1.707906e+00        -0.647150                  A
1    -1.307224e+00        -0.583841                  B
2     3.558769e-16        -0.520533                  B
3    -5.058607e-01        -0.457225                  A
4    -1.051790e-01        -0.393917                  B
5     2.955028e-01         2.075099                  C
6     6.961845e-01         1.442018                  D
7     1.136934e+00         0.175856                  B
8     1.497548e+00        -1.090306                  B
```

#### Contributing

Contributions to this project are welcome. Please feel free to fork the repository, make changes, and submit pull requests.

#### License

This project is licensed under the MIT License - see the LICENSE.md file for details.
