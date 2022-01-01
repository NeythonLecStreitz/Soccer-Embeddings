# Soccer-Embeddings

**Purpose**

The goal of this project is to create a model that takes open source data from STATSBOMB, international leaders in soccer data analytics, and generates soccer player similarities across men's and women's competitions based on play-styles. To represent the play-styles of each player, our model tokenizes their in-game actions and averages the actions across games using Genism's Doc2Vec model. 

**Motivation**

Historically, women’s soccer was banned worldwide by FIFA, the international soccer association, until 1752. The ban was in place specifically because men’s soccer organizations, such as the Football Association of England (the F.A.), were threatened by competition from an emerging popularity in women’s soccer. As a result of the ban, women’s soccer has always had to operate in the shadow of men’s soccer. In this way, part of the reason for the wage gap between men's and women's soccer is because of intentional interference by men's soccer organizations, not just because 'people like watching men's soccer more.' With that said, one solution to the wage gap is reparations in the form of promotions and monetary compensation.
The end goal then, is to represent each player as an embedded vector, allowing us to easily find the cosine similarity between players.In this way, we can take a popular men’s soccer player and find a women’s soccer player that is similar to them in the kind of actions they perform during a game. Ultimately, these comparisons could be a gateway for people who enjoy men’s soccer to get into women’s soccer, promoting the sport and women's soccer competitions. 

**Languages/Tools**

This script was written using Google's Colab Jupyter notebooks. The entire code is saved as a .ipynb file and written fully in Python. To note, this project makes use of Gensim's Word2Vec and Doc2Vec models, Numpy, Pandas, UMAP, and Plotly. 

**How To Run**

Since the entire code is written as a .ipynb, the code is separated linearly into code blocks. Run each code block from top to bottom. To get a comparison for a specific player, run this code with player_name substittuted for full player name:

top_cosine_similarities = get_similar_players(player_name, player_similarities)
print_similar_players(player_name, top_cosine_similarities)

To chart all the player comparisons, run:
plot_embeddings(avg_player_embeddings, player_metadata=enriched_player_metadata)



