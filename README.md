# jeopardy-topic-modeling

Jeopardy! is a game show in which contestants compete to answer questions the fastest against one another. Questions are placed on a game board under themes and monetary value. The theme at the top of the column in the game board represents the context of the question. The value (represented by rows) generally correlates with difficulty. In this project, I will be using topic modeling to explore trends in the Jeopardy! gameshow.

Jeopardy! is an American television game show created by Merv Griffin. The show features a quiz competition in which contestants are presented with general knowledge clues in the form of answers, and must phrase their responses in the form of questions. The original daytime version debuted on NBC on March 30, 1964, and aired until January 3, 1975. A weekly nighttime syndicated edition aired from September 1974 to September 1975, and a revival, The All-New Jeopardy!, ran on NBC from October 1978 to March 1979. The version airing as of 2021

## Dataset

The dataset can be downloaded here : https://www.reddit.com/r/datasets/comments/1uyd0t/200000_jeopardy_questions_in_a_json_file/ 

According to j-archive, the total number of Jeopardy! questions over the show's span (as of this post) is 252,583 - so this is approximately 83% of them. In particular, around the last two years of game play are missing.

The json file is an unordered list of questions where each question has

* `category` : the question category, e.g. "HISTORY"

* `value` : \\$ value of the question as string, e.g. "$200"

Note: This is "None" for Final Jeopardy! and Tiebreaker questions

* `question` : text of question

Note: This sometimes contains hyperlinks and other things messy text such as when there's a picture or video question

* `answer` : text of answer

* `round` : one of "Jeopardy!","Double Jeopardy!","Final Jeopardy!" or "Tiebreaker"

Note: Tiebreaker questions do happen but they're very rare (like once every 20 years)

* `show_number` : string of show number, e.g '4680'

* `air_date` : the show air date in format YYYY-MM-DD