# Binary Classification CNN: Cat vs Dog

Uses the professor's code from https://github.com/ubibot2000/Mask_std
(professor: Mask vs No Mask, mine: Cat vs Dog; class 0 = Cat, class 1 = Dog).

The 3 notebooks are the professor's, unchanged except the file paths (now relative folders),
`class_labels = {0: 'Cat', 1: 'Dog'}`, and the test image names.

## Dataset (on Google Drive)
The images and the trained model are too big for GitHub, so they are on Google Drive:

**DRIVE LINK: (paste your Google Drive link here)**

Download it and put the folders `origin/`, `aug/`, `predict/` and the file `model_trained_data.h5`
in the same folder as the notebooks.

- `origin/0` = 30 cat photos, `origin/1` = 30 dog photos (names `0-N.jpg` / `1-N.jpg`)
- `aug/` = augmented images made by notebook 1
- `predict/` = 20 new photos the model never trained on
- Photo source: https://github.com/nrhodes/dataset_cats_and_dogs_small

## Steps
| Step | Notebook | What it does |
|---|---|---|
| 1 | `Image Generator New(Binary).ipynb` | Augmentation: 30 variants per photo, `origin/` -> `aug/` |
| 2 | `New Fit(Binary).ipynb` | Trains the CNN, saves `model_trained_data.h5` |
| 3 | `Predict new.ipynb` | Tests the model on `predict/` |

## Results
- Test accuracy printed by the training notebook: **94.78%** (optimistic: augmented copies of the same photo
  can be in both train and test)
- On 10 brand-new photos from `predict/`: **7 of 10 correct**

```
pip install tensorflow opencv-python scikit-learn matplotlib
```
