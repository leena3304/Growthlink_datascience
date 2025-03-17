Step 1:loading Dataset
We first load the dataset and explore its structure to understand the available features. The dataset includes information such as:
Passenger details (Name, Age, Gender, Ticket Number, Cabin, Embarked Port)
Socio-economic status (Passenger Class, Fare)
Family connections (Siblings/Spouse, Parents Children aboard)
Survival Status (1 = Survived, 0 = Did Not Survive)

Step 2: Handling Missing Values
Real-world datasets often contain missing values. In this case
Age and Fare might be missing, so we replace them with the median.
Embarked (boarding location) is filled with the most common value.
Cabin has many missing values, so we convert it into a binary feature (whether the passenger had a cabin or not).
Missing data can cause errors in training, so we fill or remove them to ensure a clean dataset.

Step 3: Feature Engineering
Feature engineering helps create more meaningful variables from existing data:
Extract Title from the Name (e.g., Mr., Mrs., Miss.) since it correlates with social status.
Combine Siblings/Spouse and Parents/Children into Family Size for better representation.
Convert Cabin Information into a binary feature (Cabin Present: Yes/No).
New features improve the model’s ability to understand relationships in the data.

Step 4: Encoding Categorical Variables
Machine learning models work with numbers, so we convert categorical variables into numerical format:
Gender is converted into 0 (Male) and 1 (Female).
Embarked locations (C, Q, S) are converted into numerical features using one-hot encoding.
Title categories are also encoded.
This step ensures that categorical data can be understood by the model.

Step 5: Data Normalization
Some features (like Age and Fare) have different scales. To improve model performance:
We normalize numerical values (scale them to a similar range).
This prevents certain features from dominating the prediction.
Normalization ensures fair weightage for all features in the model.

Step 6: Splitting Data into Training and Testing Sets
The dataset is divided into training (80%) and testing (20%) subsets.
The training data is used to teach the model.
The testing data is used to check how well the model performs on unseen data.
This helps evaluate how well the model generalizes to new passengers.

Step 7: Choosing and Training a Machine Learning Model
Several models can be used for classification:

Logistic Regression (simple and interpretable)
Random Forest Classifier (handles complex patterns well)
XGBoost (powerful boosting method)
Different models are tested, and the best one is selected based on accuracy.

Step 8: Evaluating Model Performance
Here I have used Random Forest model for prediction
Once trained, the model is tested using the testing dataset. We evaluate:
Accuracy (how many predictions were correct)
Precision & Recall (performance for each class)
F1-Score (balance between precision and recall)
Evaluation ensures that the model performs well before making predictions.

Step 9: Making Predictions
After training and testing, the model can now predict survival for new passengers based on their details.
This is the final step where the model is deployed for real-world use.

Final Outcome
A well-trained classification model that predicts Titanic survival with high accuracy.
Performance evaluation ensures the model is reliable.

