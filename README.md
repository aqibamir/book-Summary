I experimented with a multpiple solutions. The first one being the naive appraoch to RAG , chunking the book into sentences and storing those sentences in a vector database. It did not work as generating a summary is different from asking questions from a book on a specific topic. 

The second approrach of doing it was using the map reduce technique. Basically all the documents are chunked into smaller segments (not into individual senteces) and seperate summaries are created for each segement. These summaries are then combined to create an overall summary of the book. This approach yielded a much better response as compared to the first one but it also suffered from the same problem as the first appraoch, passsing in the entire text. For a very large document such as the 'Crime and Punishment' book it is not feasible to generate small summaries for the entire book since the cost of doing so would be too much. 

Lastly, I landed on my final approach. It basically works by creating clusters of the entire book. The idea is that each cluster will have documents that are closely related thus enabling us to use only those segments of the book that are closely related to each other (saving us time and cost). After going through multiple iterations I landed on 53 clusters as the optimal number for generating a summary that encompases the main ideas and events of the entire book. 

# To run this notebook you would need OpenAI and Anthropic Api keys. 

~ If you face any trouble in getting the Anthropic key you can email me and I'll send you the key.

