The aim of the project is to use existing plugins and solutions, so an arbitrary number of players will be able to play on the same world map.

The key idea, as Minecraft servers currently are slow and limited to a certain amount of people, is that cluster up physically close players, and place each cluster on an other server serving the same game map, maintaining an up to date central map database.

There are further possible future improvements, the current aim of the project is MVP product.


Technical issues and solutions:

Players clustering algorithm:

Each player has a 3 dimensional coordinate position. We want to separate N players into M buckets(with an upper limit of player number in each bucket, and ideally a low sigma in the distribution of count in buckets).
We want to have players near each other be on the same server.

Initial choice will be Ward's nearest neighbhour chain algorithm. This has an O(n^2) time complexity, so ideal only for a limited number of players, however separation of clusters is quite good.

Handling multiple servers:

There is a plugin called Bungee Cord server. This is a proxy solution, which connects multiple minecraft server to a single IP, players can move between servers.

TBC


