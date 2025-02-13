
# Symptom-Based Disease Prediction Model

## Index
- Introduction
- How We Selected the Dataset
- Challenges and Considerations
- Data Refinement Process
- Methodology
- Models Implemented
- Results and Insights
- Gradio Application Development
- Future Enhancements
- Running the Application
- Contributions
- Acknowledgments

---

## Introduction
This project explores how machine learning techniques can be leveraged for **symptom-based disease prediction**. By analyzing symptoms provided by users, the model estimates the likelihood of various diseases. The project utilizes the **Symptom-Disease Prediction Dataset (SDPD)**, performing extensive preprocessing, feature engineering, and model evaluation to improve diagnostic accuracy. The ultimate objective is to develop a user-friendly web application that provides preliminary diagnoses and suggested remedies based on input symptoms.

---

## How We Selected the Dataset
We utilized the **Symptom-Disease Prediction Dataset (SDPD)**, sourced from **Mendeley Data**. This dataset was chosen due to its:
- **Comprehensive Coverage**: Links **41 diseases** to **132 symptoms**.
- **Reliability**: Endorsed by medical professionals, including the **CDC**.
- **Structured Format**: Provided in a well-organized CSV format for seamless integration with ML models.

📌 **Dataset Reference**: [DOI: 10.17632/dv5z3v2xyd.1](https://doi.org/10.17632/dv5z3v2xyd.1)

---

## Challenges and Considerations
### 1. High Dimensionality
The dataset initially contained **132 symptoms**, requiring feature selection to reduce complexity and enhance efficiency.

### 2. Imbalanced Classes
Some diseases had significantly fewer symptom reports than others, requiring techniques such as **SMOTE (Synthetic Minority Over-sampling Technique)** to balance the dataset.

### 3. Data Quality
Several symptoms had **missing values**, which required careful imputation strategies, such as **mean filling and categorical encoding**.

---

## Data Refinement Process
### 1. Feature Selection
- Removed redundant and low-impact symptom attributes.
- Identified the most predictive features through **correlation analysis**.

### 2. Data Cleaning & Preprocessing
- **Handled Missing Data**: Replaced NaN values with 0s.
- **Normalized Data**: Scaled numerical values for consistency.
- **Categorical Encoding**: Transformed categorical symptoms into numerical representations.

### 3. Exploratory Data Analysis (EDA)
- Visualized key symptom distributions.
- Examined symptom-disease relationships.
- Identified correlations between frequently occurring symptoms and diseases.

---

## Methodology
1. **Data Splitting**: Segmented dataset into training (80%), validation (10%), and test (10%) sets.
2. **Feature Engineering**: Applied **one-hot encoding**, **feature importance ranking**, and **dimensionality reduction**.
3. **Model Training & Evaluation**: Compared multiple machine learning models to determine the most effective approach.

---

## Models Implemented
We tested multiple machine learning models for performance:

### 1. Convolutional Neural Network (CNN) ✅ *Best Performing Model*
✔ High accuracy with **strong feature extraction** capabilities.  
✔ Robust against noise in symptom representation.

### 2. Multi-Layer Perceptron (MLP)
✔ Performed well but slightly lower accuracy than CNN.  
✔ Requires extensive feature engineering for optimal results.

### 3. Recurrent Neural Network (RNN) with LSTM
✔ Not ideal for symptom-based classification.  
✔ Struggled with high-dimensional symptom representation.

---

## Results and Insights
- **CNN achieved the highest accuracy**, making it the ideal choice for real-world application.
- **Feature importance analysis** revealed that some symptoms carried more predictive weight than others.
- **Data preprocessing improvements** significantly impacted overall performance.

📊 *Final Model Performance Summary:*
| Model | Accuracy |
|--------|---------|
| CNN | **92.4%** |
| MLP | 88.7% |
| RNN (LSTM) | 79.2% |

---

## Gradio Application Development
To provide an accessible interface for users, we developed a **Gradio-based web application** that allows real-time disease prediction based on symptom input.

### Features:
✔ **User-Friendly Interface**: Simple text-based symptom entry for ease of use.  
✔ **Instant Predictions**: The model outputs potential diseases in real-time.  
✔ **Multiple Symptom Input**: Users can enter multiple symptoms to improve diagnostic accuracy.  
✔ **Flagging & Feedback Mechanism**: Users can provide feedback on predictions to improve model refinement.  
✔ **Scalability**: The app is designed for **future API and cloud integration**.

### Development Process:
1. **Gradio Framework**: Utilized to create a browser-based UI with minimal dependencies.
2. **Backend Integration**: Connected the trained CNN model to process input symptoms and generate predictions.
3. **Performance Optimization**: Implemented caching and efficient model loading to ensure fast response times.

### Deployment Plan:
- **Local Testing**: Initial deployment for internal evaluation.
- **Cloud Deployment**: Plans to integrate with **AWS/GCP for scalability**.
- **Mobile Compatibility**: Optimizing UI for mobile users in future iterations.


---

## Future Enhancements
🔹 **Expand Training Data**: Incorporate larger datasets for better generalization.  
🔹 **Explainability**: Integrate **SHAP** or **LIME** to improve interpretability.  
🔹 **API Integration**: Connect with external health databases for enhanced diagnostics.  
🔹 **Deployment**: Optimize for cloud-based and mobile-friendly deployment.  

---

## Running the Application
To set up and run the disease prediction application:
```bash
# Clone the repository
git clone https://github.com/your-repo/disease-prediction.git
cd disease-prediction

# Install dependencies
pip install -r requirements.txt

# Run the application
python main.py
```
* Demo Link**: 

---

## Contributions
Developed by **AI Boot Camp Project 3 Team**:
- Anand Bhagwat
- Jean Clark
- Usha Hariharan
- Alexander Iruthaya

---

## Acknowledgments
Special thanks to our mentors and instructors for their guidance and feedback in refining this project.

