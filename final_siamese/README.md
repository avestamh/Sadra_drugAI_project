# Protein-Ligand Binding Prediction Workflow

This repository contains a machine learning workflow for predicting protein-ligand binding interactions. The following summarizes each step of the process, along with the corresponding scripts used.

---

## Summary of the Workflow

### 1. Data Extraction

Extracted molecular features from the `BindingDB_All_2D.sdf` file using the following script:

```bash
extract_bindingdb_data.py
```

### 2. Data Merging

Merged the Deloitte dataset with BindingDB features using:

```bash
preprocess_merge_data.py
```

### 3. Sequence Addition

Added protein sequences to the dataset to enhance the feature set with:

```bash
add_seq.py
```

### 4. Data Preprocessing

Performed data cleaning, transformation, and normalization using:

```bash
data_utils.py
```

### 5. Model Training

Trained the Siamese Neural Network using:

```bash
main.py
```

### 6. Inference and Evaluation

Tested the model on selected pairs and evaluated predictions.

---

## Files Overview

| **Script**                   | **Description**                                                                 |
|-------------------------------|---------------------------------------------------------------------------------|
| `extract_bindingdb_data.py`  | Extracts molecular features from BindingDB SDF files.                           |
| `preprocess_merge_data.py`   | Merges datasets to create a combined feature set for training.                 |
| `add_seq.py`                 | Adds protein sequences to the dataset to enrich features.                      |
| `data_utils.py`              | Preprocesses data, including cleaning and normalization.                       |
| `main.py`                    | Trains and evaluates the Siamese Neural Network model.                         |

---

## How to Run the Workflow

1. **Extract Features**:

   ```bash
   python extract_bindingdb_data.py
   ```

2. **Merge Datasets**:

   ```bash
   python preprocess_merge_data.py
   ```

3. **Add Protein Sequences**:

   ```bash
   python add_seq.py
   ```

4. **Preprocess Data**:

   ```bash
   python data_utils.py
   ```

5. **Train the Model**:

   ```bash
   python main.py
   ```

---

## Requirements

- **Python Libraries**: Ensure the following libraries are installed:

  ```bash
  pip install numpy pandas torch scikit-learn
  ```

---

This `README.md` provides a clear overview of the workflow and corresponding scripts. Happy coding! 🚀