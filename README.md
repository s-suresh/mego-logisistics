Mego Logistics  
by Sushma Suresh
Efficient logistics and route planning are crucial for reducing transportation costs and ensuring timely deliveries. We try to implement Simulated Annealing, a probabilistic technique for approximating global optimization.
Steps and Implementation
1. Define Cities and Coordinates
•	A dictionary stores city names with their respective latitude and longitude values.
•	The dataset includes major Indian state capitals and union territories.
•	 
2. Distance Calculation using Haversine Formula
•	The Haversine formula computes the great-circle distance between two points on Earth.
•	This ensures accurate distance measurements between any two cities.
3. Generate Initial Route
•	A random initial route is created, ensuring that:
 The tour starts and ends in Mumbai Dock.
The rest of the cities are shuffled randomly.
•	 
4. Calculate Route Distance
•	The total distance of a given route is computed by summing up pairwise distances between consecutive cities.
•	 
5. Simulated Annealing Optimization
i.	Cooling Schedule: Temperature starts high and gradually reduces based on a cooling rate.
ii.	Neighbouring Solution Generation: Two random cities (excluding Mumbai Dock) are swapped.
iii.	Acceptance Criteria:
•	If the new route is shorter, it is accepted.
•	If the new route is longer, it is accepted with some probability (to escape local optima).
i.	Iterations: The algorithm runs for 10,000 iterations to refine the solution.
•	 
6. Execution & Results
i.	The algorithm outputs:
•	The best route found.
•	The total optimized distance in km.
•	The initial (random) route distance for comparison.
🚀 Best Route:
Mumbai Dock → Gandhinagar → Daman → Panaji → Kavaratti → Thiruvananthapuram → Puducherry → Chennai → Bengaluru → Hyderabad → Bhopal → Raipur → Patna → Gangtok → Dispur → Shillong → Itanagar → Kohima → Imphal → Aizawl → Agartala → Kolkata → Bhubaneswar → Ranchi → Lucknow → New Delhi → Dehradun → Chandigarh → Shimla → Leh → Srinagar → Jammu → Jaipur → Mumbai Dock

📏 Total Optimized Distance: 12,069.80 km
📍 Initial Random Route Distance: 48,267.41 km
✨ Efficiency Gain: 🚀 ~75% distance reduction!
•	 
7. Visualization
•	Uses matplotlib to plot the optimized route on a coordinate map.
•	Each city is labeled on the plot.
•	 
Shipment Allocation:
Group items by unloading sequence: If each stop in the shipment corresponds to a specific group of items, you can organize them into distinct categories based on the unloading order.  
This code loads shipment route data, sorts the shipment stops in reverse order (from last stop to first), and saves the optimized loading plan in a new CSV file. 
 
Fuel Efficiency: 
