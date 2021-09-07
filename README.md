# Jeremiah Joseph ACM Research Coding Challenge README



## Approach
I decided to use python due  mostly to the nltk library and its usefulness in the project. I used a rules based approach in my solution. The reason why is because these sentences came from a passage in a story. When looking at existing datasets, I felt that there was not much data that would produce a good machine learning model of the sentiment. Also, because the story was relatively short and did not come with any existing sentiment scores, I felt that trying to create a machine learning model with a portion of the text seemed like a bad approach. After choosing a rules based approach, I researched and found two good rules based metrics: textblob and VADER. In my code, you can see that I compared the two. From the results I saw that the VADER seemed to be doing better at recognizing the sentiments. A reason why I believe this is the case is VADER is designed with social media texts in mind. Due to the numerous sentences that were fairly short and conversation based, my hypothesis is this design seemed to perform well. I tokenized the text based on the sentences and got a score for each sentence. I then converted the score from (-1,1) to a score from [1, 5] by evenly dividing (-1,1) to 5 equal regions. I then took the mean of that to get the overall sentiment score. 

## Performance/Analysis 
I ended up with an overall score of 3.625. This means that the text is slightly positive as a score is from [1,5] where 1 is extremely negative sentiment and 5 is extremely positive sentiment. I felt that this was a fairly good evaluation of the text as especially the second paragraph seemed to have a slightly positive tone when describing the individual. A feature of my solution is that I have a sentence by sentence breakdown of the score. In this we can see that the beginning scores seemed to be lower, which makes sense as the first paragraph details an argument. The ending scores are much higher, as towards the end the writer expresses praise for certain character traits of a person in the story. My expectations were that the scores would be slightly lower for the beginning paragraph, but the scores stayed for the most part at 2 or 3.  Overall, I felt that this approach did a fairly good job at finding the overall sentiment of the text. 

## Future Work
For future work I would likely recommend constructing a dataset and surveying people on the sentiment. This would allow for the use of a machine learning model to be implimented along with the metrics I used. This could possibly allow for even better results. 

## Sources
I did not copy any code from an existing project but here are sources which I used to help come up with my approach. <br />
1) https://monkeylearn.com/sentiment-analysis/ <br />
2) https://towardsdatascience.com/fine-grained-sentiment-analysis-in-python-part-1-2697bb111ed4 <br /> 
3) https://www.guru99.com/tokenize-words-sentences-nltk.html <br />

