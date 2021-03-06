# autoInvite
It is common for League of Legends players to join up for games with their friends, but groups of exactly four players are currently not allowed to join up together. AutoInvite is a bot that automatically invites players to a game of League of Legends with the goal of finding a fifth player for your group of four or easily inviting a large list of friends. Made of two parts: a python part to collect name data (spiderPull.py) and a c++ part to simulate mouse and keyboard input (fifth.cpp)

# spiderPull
A python script responsible for collecting and formating a .txt list of valid League of Legends summoner names (player names). Begins with a seed name specified by the user and spreads outwards using the same technique as a webcrawler: finding new player names in the recent games of the seed player. This method allows for large numbers of valid summoner names to be collected. The script relies on the "Cassiopeia" python libarary, a python port of the Riot Games API, as well as numpy. Please be sure to correctly install Cassiopeia (https://github.com/meraki-analytics/cassiopeia) and numpy (http://www.numpy.org/) before running.

# fifth.cpp
A c++ program responsible for inviting the players whose names were listed in the .txt list output by spiderPull. Accepts (x,y) locations of important buttons as input, which the user provides by clicking on them. After enough inputs have been provided, the program moves the users mouse automatically, simluating keystrokes and mouse clicks to invite one player at a time from the list.
