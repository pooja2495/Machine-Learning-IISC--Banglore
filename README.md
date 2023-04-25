Centre for infrastructure, Sustainable
Transportation and Urban Planning
Indian Institute of Science (IISc), Bengaluru


The aim of this exam is to test problem-solving skills and basic understanding of Python

Question 1

In a bicycle-sharing system, bicycles are stored at fixed docking stations throughout the city. Users can rent
bicycles from one docking station and return them to any other docking station. These systems are often used
for short trips around the city, providing users with a convenient and eco-friendly mode of transportation. A
dataset (https://drive.google.com/file/d/1yNtRCf0iQ1nP1gkwYoufjUQLW3Sslifv/view?usp=sharing ) containing 6,867 bicycle trips over one day is provided. The column descriptions are provided
below.
• trip id: Unique trip identifier.
• started at: Start time of the trip
• ended at: End time of the trip
• start lat/start lng: Latitude/Longitude of the starting depot
• end lat/end lng: Latitude/Longitude of the end depot
1. Write a function that removes all trips of duration 0 minutes and prints the following values on the
console. Mention the same values in the report.
• Maximum duration of the trip (in minutes).
• Minimum duration of the trip (in minutes).
• Total number of trips corresponding to the minimum duration.
• Percentage of total circular trips. A trip is defined as circular if it starts and ends at the same
location.
• Total runtime for the function
Hint: The question is designed to judge your basic skills in exploratory data analysis.

2. Filter the original dataset to include only the trips starting between 06:00 AM and 06:00 PM. Find
the total number of feasible pairs of trips. Two trips, A and B, are defined as a feasible pair if they
can be served in succession by the same bicycle, i.e., if the end location of trip A is the same as the
start location of trip B and the start time of the trip B is greater than or equal to the end time of the
trip A. For example, Trip Id 1733 and 1965 are feasible. In the report, mention the total feasible pairs
of trips and runtime.
Hint: The question is designed to judge your critical and analytical thinking.

3. Filter the original dataset to include only the first 100 trips (i.e., trip id 1 to 100). In the report,
mention the number of unique depots used to serve these trips. Next, find the shortest path distance
between all the depots. To do so, do the following steps:
• Download the underlying graph using the OSMnX module (https://osmnx.readthedocs.io/en/stable/) in Python.
• Find the nearest node in the graph corresponding to each depot.
• For every pair of nodes, run a shortest path algorithm (for example, Dijkstra’s ( https://networkx.org/documentation/stable/reference/algorithms/generated/networkx.algorithms.shortest_paths.weighted.dijkstra_path_length.html#networkx.algorithms.shortest_paths.weighted.dijkstra_path_length )) to
get the length of the shortest path. If the nodes are not reachable from each other, the function
should return -1.
In the report, mention the total runtime and the maximum and minimum (greater than 0) distance
