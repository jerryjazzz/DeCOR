# DeCOR
Understanding Concepts via Deep Concept-Oriented Recognition


Problem with Yelp:
    * Lots of irrelevant material when it comes to deciding what to order
Solution:
    * DeCOR - Deep Concept-Oriented Recognition
    * A quick way to process information and decide what to order and what to avoid

Method:
    * Long Short-term Memory Embedded Neural Network that really understands the concept of food
    * Essentially insert text (one sentence or 10 million reviews) and we will extract all of the food words

    * The network doesn't use explicit dictionary (or else we won't be able to discover food terms not in list)
    * Network learns to categorize each food based on context, term frequency, linguistic relationship to 
      search concept and neighboring words. The actual word is the least important aspect.

    * In many ways this is how we learn about concepts. If I gave you a sentence with a foreign food & told you 
    to find the word, most of you will be able to do it . The algorithm works the same way. 

Yelp Application:

    * Process 1.2 million reviews for top restaurants in 6 major U.S. Cities. 

    * We wanted to offer a simple and minimalist layout to tell you what to order and what to avoid:
        * Feed - Get the most recently talked about foods, rate if you enjoyed the dish as well

        * Best and Worst - best and worst dishes at the restaurant. 
            * Sentiment Analysis: 
                  We can get best foods from 5 star reviews and worst foods from 1 star reviews.
                  But most people don't like to give such extreme scores. The mass of the content is in 
                  the middle. We run sentiment analysis on each sentence and categorize as postive, 
                  neutral or negative. The corresponding foods mentiond for each sentiment are placed 
                  into Best and Worst foods. 

        * Switch - Search for another restaurant

    * Front end specifications:
        Ionic framework to create hybrid mobile application.

Accuracy and Succesful Nuances:

    * How well does this model perform? We can't just look at accuracy. Even in review's, most of the words are 
      not food words. So if the model predicts all the words to be non-food words, we would get a model that's 
      about 80% accurate. So we need to look at other metrics, specifically recall (which is how many of the 
      foods did we actually categorize as food words). Our recall was 93% based on our training set of 
      1.6 million sentences. 

    * Sammiches: The algorithm is able to identify foods that would escape a traditional food dictionary with 
      words like sammiches instead of sandwiches.

    * Differentialization: Focusing the context window allows to differentiate different sentiments behind 
    very similar or even the same words. Ex: We pigged out. We ate like pigs. We ate pigs in a blanket.

    * Noun phrases: Sure we can pick up foods but many restaurants have very spefici disher.
      Ex: Atomic burger. So we used natural language processing techniques to identify key noun phrases
      surrounding our food terms and extracting these connected pairs and triplets. 


Extension:

    * We can generalize this algorithm to completely change the way we process information. 

    * We apply this algorithm to help machines learn very difficult concepts that may seem simple to us.
      By doing so, we can make processing information very efficient. Since we have the ability to learn
      the concept the then identify subjects and patterns from those concepts without any dictionary of terms,
      we can do things like:
          * identify terms related to your search from research documents and place them on a timeline to see 
            change in trends and prevously hidden patterns
          * Or use it identify sentiment sensitive information from twiteer feeds that are key players for
            financial markets or even monitor and prevent organized crime. 
          * The applications are endless and we're very excited to start using this technology to help
            machines learn but ultimately to help us change the way we learn. 
