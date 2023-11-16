# Customer-revenue-prediction

1. **Mounting Google Drive:**
   - The script starts by mounting Google Drive to access files from the drive.

2. **Importing Libraries:**
   - The necessary libraries are imported, including NumPy, Pandas, Seaborn, Matplotlib, and TensorFlow (Keras).

3. **Loading the Dataset:**
   - The script reads a CSV file named 'online_shoppers_intention.csv' into a Pandas DataFrame (`shop`).

4. **Data Exploration:**
   - Descriptive statistics, shape, and missing value information are explored using methods like `describe()`, `shape`, and `isnull().sum()`.

5. **Correlation Analysis:**
   - A heatmap is generated to visualize the correlation between different columns in the dataset.

6. **Feature Engineering:**
   - Certain columns ('Administrative', 'Informational', 'ProductRelated_Duration') are dropped from the DataFrame (`shope`).
   - Categorical columns are identified, and dummy variables are created using `pd.get_dummies()`.

7. **Feature Selection:**
   - Redundant features are removed, and the target variable ('Revenue') is separated.

8. **Data Type Conversion:**
   - Boolean values in the dataset are converted to float32.

9. **Neural Network Model:**
   - A sequential neural network model is created using Keras.
   - Dense layers with different units and activation functions are added.
   - The model is compiled with 'adam' optimizer, 'sparse_categorical_crossentropy' loss, and 'accuracy' as a metric.

10. **Model Training:**
    - The model is trained on the data using the `fit` method with 100 epochs and a validation split of 0.1.

11. **Model Saving:**
    - The trained model is saved in the HDF5 format using `model.save()`.

12. **Summary:**
    - The code aims to build a neural network model for predicting online shoppers' intention to make a purchase based on various features.
