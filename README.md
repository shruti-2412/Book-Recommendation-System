## Book Recommendation System

### Data Description   
We've three dataset -  
• Book data – (ISBN, Book-Title, Book-Author, Year-Of-Publication, Publisher, Image-URL-S, Image-URL-M, Image-URL-L)  
• Users data - (User-ID, Location, Age)  
• Ratings data - (User-ID, ISBN, Book-Rating)   

Dataset link: https://www.kaggle.com/datasets/saurabhbagchi/books-dataset

### Summary of Project

- As the first step, we performed data preparation (i.e data cleaning and feature engineering) and EDA part.   

- After data preparation, build a recommendation system based on popularity (i.e ratings). These recommendations are usually given to every user irrespective of personal characterization. Merged book_data dataset and ratings, considering ISBNs that were explicitly rated for this recommendation system. We have listed all the top 50 books with the highest average rating but we have only selected those books whose no ratings are more than 250.

- The third step is to do Collaborative Filtering - Memory based approach was our first trial on train and test dataset which uses the memory of previous user's interactions to compute user's similarities based on items they’ve interacted with (i.e user-based approach) or compute items similarities based on the users that have interacted with them (i.e item-based approach). Our approach here is that we will only select users who have rated more than 200 books and we will only select books that are rated by more than 50 users to get more accurate results for the model and avoid outliners. Then we apply cosine similarity to make item similarity need to take the transpose of a matrix. This matrix would help in managing the train-test matrix. After all views predictions based on similarity, we find recommendation on it based on score. 

- The last step is to create a function recommend which will take the book name as input from the user and it will return 4 similar books with the author.

### Reference images  

![Screenshot (81)](https://github.com/shruti-2412/Book-Recommendation-System/assets/99483160/1b8c922b-e119-49e3-958b-983fb24aea0e)

![Screenshot (82)](https://github.com/shruti-2412/Book-Recommendation-System/assets/99483160/076c8fcd-6e21-4a4c-a4d6-cc8f5501cf8a)

![Screenshot (83)](https://github.com/shruti-2412/Book-Recommendation-System/assets/99483160/4356a401-e89a-49c0-a32e-481e1b5df56e)
