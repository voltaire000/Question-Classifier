# README
## Project Statement : Create an inquiry type classifier that will allow search engine optimization
#### The project should be able to classify between two seperate types of inquiry in order to show a basic model of what the search engine optimization classifier would look like.

## Data Collection/Cleaning/EDA
There were no missing values so those did not have to be sorted. 
<br><br>All punctuation and numbers were removed from the data as the examples i looked at the numbers and punctuation seemed  useless.
<br><br> The data has some issues coming from the reddit format that causes some words to have an overly large representation in the dataset.

## Preprocessing
data was split 50/50 as the dataset seemed large enough that it wouldn't make too big of a difference having one or the other be larger. <br><br>
 The data was lemmatized prior to having it count vectorized in order to create more meaningful word interactions. 

## Modeling
#### GaussianNB and Logistic regression are being used in order to counteract some of the innate variance present in natural language processing. 
GaussianNB specifically has a very good chance at being successful on this data as the only non Normal distribution is going to be in the words and the heavy bias should be able to fix that Logistic Regression should also be able to correct some of that heavy variance the dataset has. 
#### Random Forest Classification was also used to see if the data is overly variant so if the Random Forest Classification has too high of an accuracy score there should be some amount of evaluation of the data to see if any of the words are overly represented. This is being done to counteract some of the moderation bias in the subreddits chosen.

 GaussianNB and Logistic Regression are about equally good which is to be assumed as they are very similiar models especially for this type of data.

The models came out very accurate but it is probably just because of how variant the moderation efforts are on the seperate subreddits and the fact that the inquiry types we are looking at are so variant from one another.

## Conclusions
Reddit is probably one of the worst places to collect data for this type of inquiry classifier due to the fact that moderation and common subjects force people into specific sentence and question types. <br><br>
If you were to try to collect information from reddit it would probably be preferable to get information based on a question mark at the end of the title so that you could collect information from all variety of subreddits instead of question specific subreddits. <br><br>
From here if you wanted to continue optimizing this problem it would probably have to be either human trained or use a better data source than reddit due to how often certain words come up on the platform and the bias to younger people when the initial project statement was primarily directed at less technically literate people.