# Naveenkuamr_202401100400121 
# 🎓 Student Pass Prediction Using Random Forest

This project is a simple machine learning pipeline built with Python to predict whether students will pass or fail based on their **attendance**, **previous academic scores**, and **study hours**.

It uses a Random Forest Classifier and is designed to run in **Google Colab**, allowing users to upload their own dataset in CSV format.

---

## 📂 How It Works

1. **Upload CSV File**  
   Upload a CSV file containing student data via Colab's file uploader.

2. **Data Preprocessing**  
   - The script checks for the required columns:
     - `attendance`
     - `previous_score`
     - `study_hours`
     - `pass` (target label, should be 0/1 or 'Fail'/'Pass')
   - Rows with missing columns will trigger an error message.

3. **Model Training**  
   - A `RandomForestClassifier` from scikit-learn is used.
   - Data is split into training and testing sets (80/20 split).

4. **Evaluation**  
   - The model's performance is shown using a classification report (precision, recall, F1-score).

5. **Predictions**  
   - Predictions are made for all students in the dataset.
   - A new column `Predicted_Result` is added to the DataFrame showing "Pass" or "Fail".

---

## 📊 Example Required Dataset Format

| attendance | previous_score | study_hours | pass |
|------------|----------------|-------------|------|
| 85         | 78             | 4.5         | 1    |
| 60         | 55             | 2.0         | 0    |

- `pass`: 1 for Pass, 0 for Fail

---

## 🛠️ Requirements

- Python 3.x
- Google Colab
- Libraries:
  - `pandas`
  - `sklearn`
  - `google.colab` (for file upload in Colab)
  - `io`

---

## 🚀 How to Use

1. Open the notebook in [Google Colab](https://colab.research.google.com/)
2. Run the script cell-by-cell.
3. Upload your CSV when prompted.
4. View model performance and predictions.
5. Optionally download the resulting CSV with predicted results.

---

## 📎 Optional Enhancements

- Visualize confusion matrix
- Handle missing values more robustly
- Use label encoding if `pass` column uses "Yes"/"No"
- Export results as a downloadable CSV

---

## 📃 License

This project is open-source and free to use for educational purposes.

