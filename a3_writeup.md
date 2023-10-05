# Assignment 3 - Writeup

Assignment 3 is all about creating this natural language query system.  In order to do so, you have to write a lot of functions to retrieve infomation.  You will also have to write a function to return answers from a pattern-action list.  There is a lot of work to accomplish in this assignment, but this portion is intended for you to write about what you accomplished.

## Reflection Questions
1. In your own words describe the `search_pa_list` function.

The search_pa_list function is the part of the chat bot that connects the patterns that we have with the actual query from the user. The pa_list variable holds those patterns, and also holds whatever funtion should be used with each pattern, which makes the search-pa-list function a lot more simple. This is because the function can just call the callable function that is within the tuple with the string list, instead of having to do the extra step of finding the correct funtion to use as well.

2. What movie did you add to the `movies.py` file?  What year was it made? Any specific reason you added that movie?

I chose to add Avengers: Infinity War. It was made in 2018. I didn't really have big reason for it, it was just the first movie that popped into my mind when I realized we had to add one to the list.

3. What pattern / action did you add to the paList data structure?  Why do you think that is a useful pattern / action?

I added both the title_by_two_actors and the title_by_actors actions. They might not be the most useful actions but they do make it a quicker process to find movies that have multiple specific actors than if the title_by_actor action is used multiple times. The title_by_actors method can do everything that the title_by_two_actors can do, but the title_by_two_actors method still has use because it just gives the bot another thing that it can understand.

4. What is chatbot would you create that would be like this?  Describe why you would create it and what it would do.

I would create a chatbot like this that could go through a database of songs and find certain information depending on what is requested. The data base would hold things like the song name, singers, composers, key,etc. I would want to create this because it could be fun to use and it could help find songs that are similar to other songs, which could be useful if you want to find more songs that are like a song you like.

5. What was the most difficult portion of this assignment?

The most difficult part of this assignment by far was the title_by_actors function. It took me multiple days to complete and sometimes I had no idea how to fix the problems that were showing up. Eventually I pulled it off kind of but it took a while. The largest problem that I had, or at least the most recent one since its the only one I can remember right now is that the match function returns a list of one string with all the actors names in it, which meant it was hard to seperate them in order to use them in the search. Eventually I settled on splitting the string and adding every two adjacent strings as an element, which means it works for most cases where the actors have only a first and last name in the database, but it doesn't work if even one actor has less or more than 2 parts to their name.

6. Did you write a new assert for your pattern action?

Yes, I wrote multiple asserts for both new pattern actions. For each one, I wrote one assert that used the search_pa_list function, and one that just used the new function, so that I could have a better idea of where errors were popping up. The hardest assert to get past was the very last one, since as I said in the previous answer, the search_pa_list would return the actors as one big string, so it was hard for me to isolate each actors name.
