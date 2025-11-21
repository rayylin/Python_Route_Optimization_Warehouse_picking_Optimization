# Python Route Optimization - TSP
We use the Gene algorithm to solve the Traveling Sales Person problem and applied the solution to perform route optimization. Users enter the names or addresses they want to visit.The model turns the addresses into coordinates, calculates the distances among points, performs the Gene Algorithm, and returns the best route

# Project background infomation -
The Travelling Salesperson Problem (TSP) is defined as "Given a list of cities and the distances between each pair of cities, what is the shortest possible route that visits each city exactly once and returns to the origin city?"

We usually encounter this issue in real life. For example, I want to visit several cities, and what is the best route. In the business world, companies like FedEx need to optimize its route to save time and money, thereby providing better service.

In this project, I choose several universities in the Mid-West that I want to visit. The goal is to minimize the total distance I need to travel.

# Universities to visit
     Purdue University
     Indiana University
     University of Chicago
     Indiana State University
     Notre Dame University'
     Butler University
     UIUC
     Illinois State University

# Get the coordinates of each university
We could use geopy to get the coordinates of each university. Remember to set user_agent for the Nominatim (It's discouraged to use the default one)
I just need to input "Purdue University" and then can get the coordinates

![image](https://user-images.githubusercontent.com/58899897/194602340-cc77479b-f9d1-44ae-8543-3df01dc888e6.png)

# Visualization
We can randomly assign a sequence and see the result. 
![image](https://user-images.githubusercontent.com/58899897/194605753-76f918d9-c6a6-4092-878c-ad67db609070.png)
As the picture uses coordinates, it may not be very correct. To solve that issue, we use Folium to create a map.

![image](https://user-images.githubusercontent.com/58899897/194609537-082241d9-8e30-4c53-9803-ef5a9e1a59e3.png)

# Calculate the distance
We use the Haversine function to calculate the distances between two nodes and create a matrix to store the values.
![image](https://user-images.githubusercontent.com/58899897/194611763-e34645db-ea72-41a2-9e75-8add2416e279.png)


# solve TSP 
We use Gene algorithm to solve this problem.

# Final Result
![image](https://user-images.githubusercontent.com/58899897/194611038-406f7274-f2cc-4a7f-beca-9cf357c5587c.png)
![image](https://user-images.githubusercontent.com/58899897/194610914-47f499d9-a7e1-4b71-81c3-2546974420c3.png)

The initial distance is 1467, and the best distance after 180 iterations is 892. There is a big decrease in the total distance travel!

# warehouse picking operations
We can apply this algorithm for warehouse picking operations. 
![image](https://user-images.githubusercontent.com/58899897/198854345-37982041-5955-4084-93cb-92cee62bc4ca.png)

First we need to define the layout of warehouse

![image](https://user-images.githubusercontent.com/58899897/198861053-b93a60e8-63de-4853-8c49-6cf510f204e0.png)

The only thing we need to change is the function to calculate distance.

![image](https://user-images.githubusercontent.com/58899897/198854398-a91c8543-c8de-4df2-bca9-ad0cffc15eff.png)


Reference:
Python实现进化算法求解TSP(旅行商问题)https://zhuanlan.zhihu.com/p/153098599
