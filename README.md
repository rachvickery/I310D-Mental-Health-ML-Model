## Mental Health Assessment for University Students and Employees

In recent years, the prevalence of psychological distress among students and employees in educational institutions has been a growing concern. According to the National College Health Assessment by the American College Health Association in 2021, nearly three-quarters of students reported experiencing moderate to severe psychological distress. Post-COVID, this issue has exacerbated, highlighting the need for accessible mental health resources, especially in universities.

### Project Objective
Our group aimed to tackle the challenge of limited mental health resources in universities. Leveraging the "Social Media and Mental Health" dataset from Kaggle, we delved into survey data on social media usage and mental health screening questions. The primary goal was to develop a machine learning model capable of predicting mental health risk among university students and employees. By analyzing this data, we sought to identify individuals who might benefit from targeted mental health resources.

### Dataset Description
#### Original Dataset (Dataset 1)
- **Categories Included:**
  - Personal Information: Age, Gender, Relationship Status, Occupation, Affiliation
  - Social Media Usage: Platforms Used, Time Spent on Social Media
  - Mental Health Screening: ADHD, Anxiety, Depression, Self-esteem (Likert Scale - 1 to 5)
  
#### Data Preprocessing Steps:
- **Column Management:**
  - Simplified column names for clarity and ease of understanding.
  - Rearranged questions by grouping related sections (ADHD, anxiety, depression, self-esteem).
- **Filtering and Dropping:**
  - Filtered the dataset to include only university-affiliated individuals (students or employees).
  - Removed irrelevant columns like index, timestamp, occupation, and affiliation.
- **Data Transformation:**
  - Modified data types for appropriate machine learning model training (e.g., converting string inputs to numerical values).
- **Outcome Creation:**
  - Constructed an outcome column based on a total score of mental health screening questions and social media usage.
  - Assigned a binary classification (0 or 1) for individuals deemed at-risk or not at-risk based on a cutoff score of 45.

#### Synthetic Dataset (Test #2)
- **Purpose:** To further evaluate the model's performance in complex scenarios.
- **Characteristics:**
  - Emphasizes individual section-based averages, particularly for depression-related questions.
  - Introduces cases where participants with total scores below 45 might still be categorized as "at risk" based on specific section averages.
  - Utilizes a redesigned binary outcome (0 for not at risk, 1 for risk) with emphasis on section-based averages signaling mental health risk.

### Tools and Technologies
Our analysis primarily involved Python on Google Colab. We utilized various libraries, including Pandas, Numpy, Matplotlib, Seaborn, and DataPrep EDA, for data visualization, analysis, and preprocessing.

### Conclusion
Our efforts focused on creating a predictive model to identify individuals at potential mental health risk among university students and employees. By leveraging machine learning on the provided dataset and a synthetic test dataset, we aimed to enhance the accessibility and effectiveness of mental health resources in educational settings.
