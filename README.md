# Airline and Airport Review Sentiment Analysis


## Overview
This project implements a Naive Bayes classifier for sentiment analysis of airline, airport, lounge, and seat reviews. The system analyzes customer reviews across multiple categories and predicts ratings based on textual content.


## Features
- Multi-category sentiment analysis
- Custom tokenization with phrase capture
- Handling of compound sentences with 'but' and 'and' conjunctions
- Rating prediction for multiple aspects:
  - Overall experience
  - Queuing efficiency
  - Seat comfort
  - Cabin quality
  - Staff service
  - Value for money
  - Food and beverages
  - Shopping experience
  - WiFi connectivity
  - Hygiene standards
  - Entertainment options


## Dependencies
- pandas
- nltk
- re (regular expressions)
- math
- collections (Counter, defaultdict)


## Data Structure
The system processes four main datasets:
- Seat-related reviews
- Airport lounge reviews
- Airline service reviews
- Airport facility reviews


## Key Components


### 1. Data Preprocessing
- Missing value handling
- Text normalization
- Custom tokenization for capturing multi-word phrases
- Stop word removal


### 2. Feature Engineering
- Phrase detection for common expressions
- Special handling of compound sentences
- Weighted tokenization for sentences with 'but' clauses


### 3. Rating System
The model calculates ratings on a 1-5 scale across different categories using:
- Prior probability calculation
- Likelihood computation
- Posterior probability estimation
- Overall sentiment score aggregation


### 4. Category Mappings
The system maps various aspects of reviews to standardized categories:
- Lounge reviews: comfort, staff service, beverages
- Airport reviews: queuing, terminal seating, cleanliness
- Airline reviews: seat comfort, cabin staff, entertainment
- Seat reviews: legroom, viewing experience


## Model Features


### Tokenization
- Captures specific phrases like "not comfortable", "excellent service"
- Handles negations and compound sentences
- Removes punctuation and converts to lowercase
- Filters stop words


### Rating Prediction
- Calculates likelihood using word frequencies
- Applies Naive Bayes classification
- Handles edge cases with smoothing
- Provides category-specific ratings


## Performance Notes
- Uses logarithmic probabilities to prevent underflow
- Implements smoothing for unseen words
- Handles missing values gracefully
- Weights words differently based on sentence structure


## Future Improvements
- Implementation of cross-validation
- Addition of more sophisticated feature engineering
- Integration of deep learning models
- Enhanced handling of specialized vocabulary
