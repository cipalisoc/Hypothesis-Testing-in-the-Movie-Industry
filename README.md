# The Most Successful Films Produced
## Analyzing Factors in Film that Make Successful Movies

Christian Palisoc
 
For this project, I was tasked to produce a MySQL database on Movies from a subset of IMDB's publicly available dataset. The project is divided into four parts, all outlined below. Ultimately, this database was used to analyze what makes a movie successful, and to provide recommendations to the stakeholder on how to make a successful movie.

# Data Source
Overview/Data Dictionary: https://www.imdb.com/interfaces/  
Downloads page: https://datasets.imdbws.com/  
The Movie Data Base (TMDB): https://www.themoviedb.org/

# Part 1
The first part of the the project consisted of downloading several files from IMDB’s movie data set and filter/clean the subset of moves requested by the stakeholder. Per stakeholder requirements, I only included information for movies based on the following specifcations:  
- Exclude any movie with missing values for genre or runtime
- Include only full-length movies (titleType = "movie").
- Include only fictional movies (not from documentary genre)
- Include only movies that were released 2000 - 2021 (include 2000 and 2021)
- Include only movies that were released in the United States

# Part 2
This portion of the project required the addition of box office revenue and profit, MPAA Rating, and budget to my IMDB data. The data was extracted from The Movie Data Base (TMDB) by constructing an API function and tested on movies that started in 2000 and 2001. In order to ensure your function for extracting movie data from TMDB is worked, the function was tested on  2 movie IDs: tt0848228 ("The Avengers") and tt0332280 ("The Notebook"), which ran without error and returned the correct movie's data for both test IDs.  

Some exploratory data analysis was performed and produced the following insights:

![ratings](https://github.com/cipalisoc/Project3/blob/main/number%20of%20movies%20by%20rating.jpg?raw=true)  
The visual depicts the number of movies broken down by MPAA rating (certification) produced in 2000 and 2001.  

Of the movies produced in 2000 and 2001, `1114` movies had some valid financial information (values > 0 for budget OR revenue). Furthermore, the average revenue per MPAA rating are as follows:
