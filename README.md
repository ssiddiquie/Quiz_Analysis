
# Overview

Personalized Student Recommendations is a Python-based solution that analyzes student quiz performance to offer tailored recommendations for improving their preparation. This solution focuses on providing actionable insights based on past performance, highlighting strengths and weaknesses across various topics and difficulty levels. It can be used to guide students as they prepare for exams like NEET (National Eligibility cum Entrance Test).

The solution processes two datasets—Current Quiz Data and Historical Quiz Data—then generates insights, highlights performance trends, and makes recommendations that help students focus on areas where they need improvement.
Features

    Quiz Performance Analysis: Analyzes a student’s performance across different quizzes and identifies areas of strength and weakness.
    Personalized Recommendations: Suggests topics, question types, and difficulty levels for further study to optimize preparation.
    Historical Performance Tracking: Evaluates performance across the last 5 quizzes to identify improvement trends and consistency.
    Student Persona Development: Categorizes students into different personas based on quiz data patterns (e.g., Strong in certain topics, Weak in others).
    Probabilistic Rank Prediction (Bonus): Predicts the student's NEET rank based on their performance in the quizzes and previous years' NEET data.

# Data Overview

# API Endpoint: /submission_data
1. Current Quiz Data

Contains details of the user’s latest quiz submission, including:

    Question IDs
    Topics covered
    Responses (including question, selected answer, etc.)

# API Endpoint: /history_data
2. Historical Quiz Data

Contains performance data from the last 5 quizzes for each user, including:

    User scores
    Response maps (Mapping Question IDs to Selected Option IDs)

# Approach
Data Analysis

    Explore Schema: The first step is to load and examine the structure of the data. We look for trends in performance (e.g., frequent wrong answers for certain topics or question types) to identify where students are struggling.

    Performance Metrics: Key metrics like accuracy, response time, and topic-wise performance are extracted to gauge strengths and weaknesses.

    Pattern Identification: By analyzing historical data, patterns emerge about topics, question types, and difficulty levels that the student consistently performs poorly on.

Insight Generation

    Weak Areas: Based on the student’s current and historical performance, we identify areas where they need improvement (e.g., biology topics like genetics, or difficult question types).
    Improvement Trends: Track improvements over multiple quizzes to suggest areas where the student has made progress.

Recommendations

    Suggest targeted practice for weak areas based on their recent quiz history.
    Recommend revisiting questions from higher difficulty levels or specific topics that need more focus.

# Bonus Feature: Probabilistic Rank Prediction

We incorporate past NEET performance data to estimate the student’s rank using a probabilistic model based on their quiz performance.
Installation
Prerequisites

### Ensure that you have the following dependencies installed:

    Python 3.x
    Libraries: pandas, numpy, scikit-learn, matplotlib, seaborn, requests (for API calls)

You can install the required libraries using pip:

pip install pandas numpy scikit-learn matplotlib seaborn requests

### Setup

    Clone this repository:

git clone https://github.com/your-repository/personalized-student-recommendations.git
cd personalized-student-recommendations

    Run the script:

python recommend.py

The script will analyze the student’s quiz data and generate recommendations based on their performance.
Usage

    Input Data: The script fetches data through API calls to the /quiz_submission_data and /historical_quiz_data endpoints. Make sure to have access to the correct API or substitute with local data.
    Analysis: The script processes the quiz data, analyzes trends, and provides insights in the form of recommendations.
    Output: The output will be a set of personalized recommendations for the user, focusing on weak topics and strategies for improvement.


Feel free to fork this repository, submit issues, or create pull requests to improve the analysis and recommendations. Contributions are welcome!
License
