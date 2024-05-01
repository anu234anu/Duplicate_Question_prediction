Statement -  Duplicate Question Detection

 Tools Used:
- Google Colab
- Beautiful Soup
- NLTK
- Numpy, Pandas
- Matplotlib, Seaborn

  
  Steps followed:
1. Import required libraries and dataset.
2. Preprocessing:
 1. Convert into lower case and remove extra spaces.
 2. Replace special characters with String equivalents.
 3. Replace numbers with String equivalents.
 4. Replace decontracting words with the String equivalents.
     E.g. ain’t = am not
 5. Remove HTML tags and punctuations.
3. Calculate the length and number of words in both the questions for each row.
4. Calculate the common words in both questions and the total number of words in both questions.
5. Fetch token features:
 1. Convert sentence into tokens.
 2. Get non-stop words in questions.
 3. Get stopwords in questions.
 4. Get the common non-stopwords from Question pair.
 5. Get the common stopwords from Question pair.
 6. Get the common Tokens from Question pair.
 7. Check if the first and last words of both questions are same or not.
6. Calculate three length-related features:
  ● Absolute length difference between the two questions.
  ● Average token length of both questions.
  ● Length of the longest common substring divided by the minimum length of
the two questions plus 1.
7. Determine the fuzz_ratio, partial_ratio, token_sort_ratio, token_set_ratio.
8. 8. Convert question pair into vectors using CountVectorizer.
9. Split the data into training and testing sets.
10. Compile and train neural network model.
11. Evaluate the model.
