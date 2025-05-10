# SMART MARKETING SITUATIONAL CONSUMER BEHAVIOR USING INDOBERT-BASED SENTIMENT ANALYSIS
## Research Flow
![image](https://github.com/user-attachments/assets/f4d92661-e09d-4109-a9c1-bae392a45bf9)


This diagram illustrates the workflow in sentiment analysis using the IndoBERT model.
1. Crawling Data
This is the process of collecting raw data, typically from social media, websites, or online reviews. In this context, it's likely customer reviews or opinions relevant to sentiment analysis.

2. Dataset
The collected data is stored in a structured format (e.g., CSV, JSON) as a dataset, ready to be processed.

3. Pre-processing
This phase involves preparing the text data so it can be effectively analyzed by the model. Steps include:
- Text Cleaning: Removing irrelevant characters, punctuation, or HTML tags.
- Text Normalization: Converting text into a standardized format (e.g., lowercasing, correcting slang or typos).
- Tokenization: Splitting text into individual words or tokens.
- Stopword Removal: Removing common words (like "and", "the") that don’t carry significant meaning.
- Stemming: Reducing words to their root form (e.g., "running" → "run").
- Identification Faktor: Identifying relevant factors or features from the text that may affect sentiment.

4. Model Train & Test
Using the pre-processed data to train and test the model:
IndoBERT & Hyperparameter Tuning: Utilizing the IndoBERT model (a BERT variant trained on Indonesian text) and fine-tuning its parameters to improve performance.

5. Model Evaluation
After training, the model is evaluated using metrics:
Confusion Matrix: A table used to measure the performance of a classification model, showing true/false positives and negatives.

6. Implementation & Results
The final step:
Smart Marketing Solutions: Using the insights from sentiment analysis to support decision-making, particularly for targeted marketing strategies.


## Dataset
Data that has been crawled previously is preprocessed so that it is ready to be processed in the algorithm used, there are 6 stages of data preprocessing used in this research.

![image](https://github.com/user-attachments/assets/a9b61d12-2f96-47a6-a93c-daa527568075)


## Pre-processing
### Text Cleaning
Text cleaning is used to clean raw text data from irrelevant elements such as mentions (@), hashtags (#), retweets (RT), links, numbers, or other special symbols. This process ensures that the text contains only the main information that can be used for analyzing consumer behavior related to Mie Gacoan.

![image](https://github.com/user-attachments/assets/12f385fe-4de4-43f1-97a8-22927f898fe4)

### Text Normalization
Text normalization is used to convert informal or slang words into their standard forms based on the formal Indonesian language dictionary. This step is important to improve the accuracy of factor analysis by ensuring that words are consistent and easily recognized by the IndoBERT model.

![image](https://github.com/user-attachments/assets/c8270dda-55a4-42d2-9732-976edf0a2c8d)

### Tokenization
Tokenization is used to break the text into individual word units (tokens). This process enables deeper analysis of word or phrase patterns that are relevant for identifying factors in consumer behavior (physical, psychological, economic, or non-factor).

![image](https://github.com/user-attachments/assets/a1d88f89-19a3-4f05-85ce-c530961ea001)

### Stopwords
Stopword removal is used to eliminate common words (stopwords) that do not provide significant informational value, such as “yang,” “dan,” or “dengan.” This step aims to focus on important words that contribute more to the identification of factors or categories in the analysis.

![image](https://github.com/user-attachments/assets/fae0c767-ae4b-42a6-9c5f-2f2ff4d10478)

## Stemming
Stemming is used to transform a word into its root form using a stemming algorithm. For example, the word "makanannya" is changed to "makan." The main goal is to simplify word analysis so that it aligns better with the list of keywords in a dictionary of factors (physical, psychological, economic).

![image](https://github.com/user-attachments/assets/4f8f389a-5d55-4980-85d9-7c9088fbce79)

## Factor Identification
Factor identification is used to match the cleaned and processed text against a factor dictionary that includes physical, psychological, and economic categories. This step aims to identify the dominant factors in each consumer review, allowing for the development of specific and targeted marketing solutions.

![image](https://github.com/user-attachments/assets/15a7a70d-5452-44ee-b995-8b091cc65394)

## Train 
### Classification report 
From the classification model with four classes: Faktor Fisik, Faktor Psikologis, Faktor Ekonomi, and Bukan Faktor, the model achieved an overall accuracy of 0.95, meaning that 95% of all predictions made by the model were correct.
In terms of precision, the highest score was achieved in Faktor Psikologis (1.00), followed by Faktor Ekonomi and Bukan Faktor (both 0.96), indicating that the model is very precise in identifying these categories. However, Faktor Fisik had a slightly lower precision (0.75), suggesting some false positives in this class.
For recall, the model performed exceptionally well in detecting Faktor Fisik (1.00), meaning it identified all actual instances of this class correctly. Faktor Ekonomi and Bukan Faktor also showed strong recall scores (0.96 and 0.97 respectively), while Faktor Psikologis had a slightly lower recall (0.90), indicating some actual instances were missed.
F1-score, which balances precision and recall, was highest in Faktor Ekonomi and Bukan Faktor (both 0.96), followed closely by Faktor Psikologis (0.95). Faktor Fisik had a lower F1-score of 0.86, reflecting the trade-off from its lower precision.
The macro average F1-score was 0.93, reflecting the model's balanced performance across all classes regardless of their frequency. The weighted average F1-score was 0.95, indicating the model’s strong performance especially considering class imbalances — with Bukan Faktor making up the majority of the data.
Overall, the model demonstrated excellent performance, particularly in predicting Faktor Ekonomi and Bukan Faktor, with some room for improvement in the precision of Faktor Fisik predictions.

![image](https://github.com/user-attachments/assets/71bad560-e0fd-410d-9dfa-124aba3d5b6f)


### Training, Validation, and Test Accuracy
The graph displays the training, validation, and test accuracy across 10 training epochs.
- Training Accuracy (blue line with circles) shows a consistent increase from around 59% at epoch 1 to approximately 98% by epoch 9 and 10, indicating that the model effectively learned from the training data.
- Validation Accuracy (green line with squares) improves sharply until epoch 4 (around 94%), then stabilizes with slight fluctuations through to epoch 10. This pattern suggests a potential overfitting trend - - -- starting from around epoch 6, where the model continues to improve on training data but not on unseen validation data.
- Test Accuracy (red dashed line) is fixed at around 95%, suggesting that the model generalizes well on completely unseen data. The consistent test performance is a strong indicator of the model's robustness.

Insights:
- The steep rise in both training and validation accuracy during early epochs reflects rapid learning by the model.
- After epoch 6, a widening gap between training and validation accuracy becomes evident, which can be interpreted as mild overfitting.
- Despite this, the test accuracy remains high, which implies that the model maintains strong generalization ability.
- The optimal model may have emerged between epoch 4 and epoch 6, balancing both training and validation performance effectively.

![image](https://github.com/user-attachments/assets/7219cf0c-7b20-41a0-80fa-bfdf7b5616f6)


## Evaluation model
### Confusion matrix 
The confusion matrix above illustrates the classification performance of the IndoBERT model on the test dataset across four categories: Faktor Fisik, Faktor Psikologis, Faktor Ekonomi, and Bukan Faktor. The model demonstrates strong performance, particularly in correctly identifying instances of the Bukan Faktor class, with 86 out of 89 samples classified correctly. Similarly, it performs well in recognizing Faktor Ekonomi with 27 correct predictions and only 1 misclassified as Bukan Faktor. For Faktor Psikologis, the model accurately predicted 26 instances, while misclassifying 3 of them as Bukan Faktor. The classification for Faktor Fisik is nearly perfect, with all 6 samples correctly identified and no misclassifications.

The results suggest that the model is highly effective at distinguishing between the different factor categories, especially among the three core categories (physical, psychological, and economic factors). Notably, most misclassifications involved incorrectly predicting actual factor-related inputs as Bukan Faktor, indicating a slight conservative bias in the model — it sometimes errs on the side of assuming an input is not a factor at all. However, there are very few cross-category errors (e.g., psychological predicted as economic), which implies that the model has learned clear boundaries between factor types.

![image](https://github.com/user-attachments/assets/0e745bb4-3644-41c2-9df6-4973e4fe08e4)


### Smart Marketing Solutions
![image](https://github.com/user-attachments/assets/5aecc609-361f-4762-b2d3-66637e289e7e)


The dominant sentiment category identified is the Psychological Factor, indicating that consumer behavior in choosing products is influenced by emotional or psychological aspects. This aligns with the analysis results, which show that psychological factors play a significant role in the purchasing decisions of Mie Gacoan consumers. Based on these findings, the proposed marketing solution focuses on emotion-based marketing, aiming to strengthen consumers’ emotional connection with the Mie Gacoan brand. Marketing campaigns that highlight happiness, satisfaction, and personalized offers can enhance customer loyalty. Additionally, the use of visual content that links the product to emotional values is expected to further reinforce consumer appeal, potentially increasing customer satisfaction and boosting sales conversion for Mie Gacoan.
