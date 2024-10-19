I implemented a solution to the Traveling Salesman Problem (TSP) using Python to optimize the route for 
visiting all college houses at Penn to hang up posters for our Soundworks Tap Factory dance group’s semester show. 

The first step was data preparation: I collected latitude and longitude coordinates for each college house and 
stored them in a list of tuples. Using the ‘geopy’ library, I calculated the haversine distance between each 
pair of locations to create a distance matrix, which was used as input for the optimization.

The second step was implementing the solution: I defined the problem using Google’s OR-Tools package, 
specifying one person walking the route and setting a single starting/ending dorm. I created a custom callback 
function to compute the distance between locations using the distance matrix. OR-Tools then computed the 
near-optimal path based on a nearest neighbors approach, minimizing the total travel distance.

The third step was creating a visualization: After obtaining the route, I visualized the path using ‘folium’. 
I plotted markers for each location on a map and drew lines connecting them according to the computed shortest route.

This approach saved significant time, allowing me to complete the task more efficiently and conserve energy for our performance.

Here is a picture of the output of the map:

<img width="736" alt="Screenshot 2024-10-19 at 11 16 17 AM" src="https://github.com/user-attachments/assets/1130fbcc-1431-4b0f-bedd-0f88a39139a6">
