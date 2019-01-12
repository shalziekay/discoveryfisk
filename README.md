# Coding Bootcamp Articles
## Authors: Kunapuli, Shalini, McQuarrie Francie, & Schnell, Krista
### Date: Fall 2018

This research project aimed to create a data set of articles tagged with `Codingbootcamp` on the website [Medium](https://medium.com/).   
The original goal was to attempt to analyze the articles to see if we could determine the author's motivations for attending a coding bootcamp instead of the traditional four year college degree route, to supplement Krista's sociological research.   

However, after some initial analysis, we realized that most of the coding bootcamp articles were less about *why* people attended bootcamp, and more about their experiences *during* bootcamp (along the lines of "Here's what project we worked on today"). Additionally, Krista's research focus shifted away from this topic.  

Since we had already collected the data, we decided to finish what analysis we could on the articles.  We investigated how many bootcamps each article mentioned, who published the article (self published or a bootcamp itself?), the number of claps of each article (a measure of popularity), attempted to predict the gender of the author by name, and whether there were any publishing differences among gendered authors. 

### Tools
* [Python](https://docs.python.org/3/) programming language for collection and analysis.
* [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/) parsing package.
* [Jupyter Notebooks](https://jupyter.org/) to organize data collection and analysis.
* [Pandas](https://pandas.pydata.org/pandas-docs/stable/) to store and manipulate the collected articles.
* [Seaborn](https://seaborn.pydata.org/) for visualization.
* [Langdetect](https://pypi.org/project/langdetect/) for detecting language.

### Contents
* `article_data_collection.ipynb`: Notebook with code that scraped the articles and their meta data from the Medium website.
* `article_analysis.ipynb`: Notebook with code that analyzes and describes different aspects of each article.
* `articles_with_claps_and_gender.csv`: CSV of collected article information as well as the number of claps each artcile recieved and predictions about gender. 

| Column Name      | Data Type       | Description                             |
|------------------|-----------------|-----------------------------------------|
| author           | string          | Author name                             |
| author_bio       | string          | Short biography of author               |
| title            | string          | Article title                           |
| date             | string          | Article publish date                    |
| publisher        | string          | Article publisher                       |
| text             | string          | Full text of article                    |
| tags             | string          | List of tags attached to article        |
| url              | string          | Article url                             |
| score            | int             | "Relevancy" score of article            |
| bootcamps        | list of strings | All bootcamp names mentioned in article |
| num_bootcamps    | int             | Number of bootcamps mentioned           |
| claps 2019-01-02 | str             | Number of claps given to article        |
| first name       | str             | first name of author                    |
| prob_female      | float           | Probability that author is female       |
| prob_male        | float           | Probability that author is male         |

* `babynames.zip`: File of baby names data from Social Security (collected from [here](http://www.ds100.org/fa18/assets/lectures/lec02/02-case-study.nbconvert.html) and [here](http://www.ds100.org/fa18/assets/lectures/lec03/03-case-study.html))
* `bootcamp_list.csv`: List of major coding bootcamps (some have sinced shut down but their repulation while open gains them a spot on the list)
* `codingbootcamp_articles_info.csv`: Intial data collected about each article .

| Column Name      | Data Type       | Description                             |
|------------------|-----------------|-----------------------------------------|
| author           | string          | Author name                             |
| author_bio       | string          | Short biography of author               |
| title            | string          | Article title                           |
| date             | string          | Article publish date                    |
| publisher        | string          | Article publisher                       |
| text             | string          | Full text of article                    |
| tags             | string          | List of tags attached to article        |
| url              | string          | Article url                             |
| score            | int             | "Relevancy" score of article            |

* `non_english_bootcamp_articles.csv`: List of all articles collected that were predicted to be written in a language other than English. These were removed for our analysis but preserved in a separate file in case of future interest.

| Column Name      | Data Type       | Description                             |
|------------------|-----------------|-----------------------------------------|
| author           | string          | Author name                             |
| author_bio       | string          | Short biography of author               |
| title            | string          | Article title                           |
| date             | string          | Article publish date                    |
| publisher        | string          | Article publisher                       |
| text             | string          | Full text of article                    |
| tags             | string          | List of tags attached to article        |
| url              | string          | Article url                             |
| is_english       | bool            | Is the article written in English?      |

### Limitations
Part of this research attempted to predict the gender of an author using a dataset of baby names from the Social Security Administration. However, most of the names present in this dataset are of Western origin (since its data on United States born babies), so authors with unusual non-Western names might have been marked as "Unknown" gender due to lack of proper data. 
