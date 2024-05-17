# Book-Recommendation-System
Book Recommendation System  - NLP

# Darwin's Bibliography: A Content-Based Book Recommendation System

![Charles Darwin](https://assets.datacamp.com/production/project_607/img/CharlesDarwin.jpg)

## Project Overview

This project aims to build a content-based book recommendation system using Charles Darwin's bibliography. The goal is to determine how closely related his books are to each other based on their discussed topics. This system can help readers find books with similar content, providing insights into Darwin's works and enhancing the reading experience.

## Methodology

### Data Collection
The dataset was manually collected from [Project Gutenberg](https://www.gutenberg.org/). It includes multiple books written by Charles Darwin, available in plain text format.

### Data Preprocessing
The text was then cleaned by removing non-alphanumeric characters to standardize it. Next, the text was tokenized, converting it into individual words. Common English stop words were removed to focus on meaningful content. Finally, stemming was applied using the Porter Stemmer to reduce words to their root form, grouping similar words together for more accurate analysis.

### Model Building
- **Bag-of-Words Model:** Created a dictionary of all unique words and transformed each book into a list of word occurrences.
- **TF-IDF Model:** Applied Term Frequency-Inverse Document Frequency to identify words that are important within a book but not across all books, providing a better understanding of unique content.
- **Cosine Similarity:** Calculated pairwise similarity between books based on their TF-IDF representations.
- **Similarity Matrix:** Constructed a matrix showing the similarity scores between all pairs of books.
- **Bar Chart:** Displayed the books most similar to *On the Origin of Species*.
- **Dendrogram:** Visualized overall book similarities using hierarchical clustering to identify groups of related books.

### Key Findings
The content-based recommendation system successfully identified similarities between Darwin's books. For instance, books like *The Variation of Animals and Plants under Domestication* and *The Descent of Man, and Selection in Relation to Sex* were found to be closely related to *On the Origin of Species*. This makes sense as these books discuss similar concepts such as selection and domestication.
- The similarity matrix provides a comprehensive view of how Darwin's books relate to each other.
- The bar chart and dendrogram offer clear visualizations of book similarities, helping readers choose their next book based on content.

## Conclusion

This project demonstrates the effectiveness of content-based recommendation systems in text-heavy datasets. By leveraging the full text of Darwin's works, we built a model that provides insightful recommendations and deepens the understanding of his bibliography. Such a system can be extended to other authors or collections of texts, showcasing its versatility and potential applications in various domains.
