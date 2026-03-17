Ex.No.6 Development of Python Code Compatible with Multiple AI Tools

# Aim: 

Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights with Multiple AI Tools.

# Explanation:

Develop a python code that integrates multiple AI tool by interacting with their APIs.
Compare outputs from different APIs.
Analyze the response and the Output.

The aim is to understand how to request help from AI tools for tasks like writing Python code, integrating with APIs, comparing outputs, and generating actionable insights.

# Program:
```
from nltk.sentiment import SentimentIntensityAnalyzer
import nltk

nltk.download('vader_lexicon')

### Simulated AI-generated text
generated_text = "This smartphone offers outstanding battery life and an intelligent AI camera that captures stunning photos."

print("Generated Review:\n")
print(generated_text)

### Sentiment analysis
sia = SentimentIntensityAnalyzer()
sentiment = sia.polarity_scores(generated_text)

print("\nSentiment Analysis:")
print(sentiment)

### Insight generation
if sentiment['compound'] > 0:
    print("\nInsight: The review is positive and suitable for marketing promotion.")
else:
    print("\nInsight: The review tone is neutral or negative.")

```

# Result:

#### Input 1: 
This smartphone offers outstanding battery life and an intelligent AI camera that captures stunning photos.

#### Output: 
Generated Review: This smartphone offers outstanding battery life and an intelligent AI camera that captures stunning photos.

Sentiment Analysis:
{'neg': 0.0, 'neu': 0.556, 'pos': 0.444, 'compound': 0.8625}

Insight: The review is positive and suitable for marketing promotion.

#### Input 2:
This smartphone struggles with battery life, often needing frequent charging throughout the day. The so-called AI camera is inconsistent and fails to deliver quality photos, especially in challenging lighting conditions.

#### Output: 
Generated Review: This smartphone struggles with battery life, often needing frequent charging throughout the day. The so-called AI camera is inconsistent and fails to deliver quality photos, especially in challenging lighting conditions.

Sentiment Analysis:
{'neg': 0.155, 'neu': 0.79, 'pos': 0.055, 'compound': -0.5302}

Insight: The review tone is neutral or negative.



