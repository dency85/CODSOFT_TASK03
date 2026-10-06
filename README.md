# Iris Flower Classifier (Beginner Project)

This project uses the supplied `IRIS.csv` file to classify a flower as one of three Iris species from four measurements:

- `sepal_length` and `sepal_width`
- `petal_length` and `petal_width`

The species names are stored in the CSV's `species` column. The supplied dataset is included in this project folder, so the program reads it directly without a download.

## 1. What you need

- Python 3.9 or newer
- A terminal (PowerShell, Command Prompt, or the terminal in VS Code)

## 2. Set up the project

Open a terminal in this project folder and run:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

If PowerShell blocks activation, skip that command and use `.venv\Scripts\python.exe` in place of `python` below.

## 3. Run the classifier

```powershell
python iris_classifier.py
```

The script finds `IRIS.csv` beside itself, trains the model, then prints held-out accuracy, a confusion matrix, and per-species scores. It also predicts one example flower.

## How the project works

1. **Read the CSV:** the program loads the four numeric measurements and the species text label from each row.
2. **Split the examples:** 80% are used for learning; 20% are held back to evaluate the model.
3. **Scale the measurements:** this puts all four measurements on comparable scales.
4. **Train a KNN model:** it predicts a species by looking at the five nearest training flowers.
5. **Evaluate:** predictions are compared with the known species in the held-back examples.

The accuracy is an estimate from one split of this dataset, not a guarantee about every flower. Keep the CSV in the project folder when running the script. It must have the column names `sepal_length`, `sepal_width`, `petal_length`, `petal_width`, and `species`.

## Try your own flower

Edit `sample_flower` in `iris_classifier.py`. Put four centimeter measurements in this order: sepal length, sepal width, petal length, petal width.

## Project files

- `IRIS.csv` — your supplied flower dataset
- `iris_classifier.py` — the commented program
- `requirements.txt` — required third-party library
