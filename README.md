# TDIRP

This is a benchmark for the time-dependent inventory routing problem. 

The inventory routing problem (IRP) is the integration of two subproblems of the supply chain: inventory management and routing. It is set in a network where a supplier is responsible for the replenishment and the distrubtion of a set of clients in a time horizon. The time-dependent IRP (TDIRP) is of its routing component, where travelling times between two locations do not only depend on the departure and arrival locations, but on the time of departure as well. 

Travelling time functions in this benchmark are constant piece-wise functions. They are decomposed into a set of time steps, where the travelling time for each time step is constant. 

The benchmark is composed of 250 instances. The different parameters of the benchmark are the: 

  - Size of time horizon: {3,6} periods
  - Number of clients: {5,10,15,20,25,30} for instances with 3 periods and {5,10,15,20} for instances with 6 periods. 
  - Number of time steps: {1,12,30,60,120}. 
  
Each combination of these parameters have 5 different instances. 

The instances are divised into two files: H3 for instances with a time horizon of 3 periods and H6 for instances with a time horizon of 6 periods.

The name of an instances is as follows: inst_"number of clients"_"number of time steps"_"the number of the instance".txt 

The text files are written as follows: 

information about the network:
number_of_locations(number_of_clients_+_1_supplier)   number_of_periods   capacity_of_the_vehicle   number_of_time_steps  duration_of_time_step   travel_time_constraint

information about the supplier:
index_of_the_supplier=1   initial_inventory   quantity_produced_period_1   ...   quantity_produced_last_period  holding_cost

information about the client:  each line represent the information of a client
index_of_client_1=2   initial_invnetory   maximum_inventory   minimum_inventory   demand_period_1   ...   demand_last_period  holding_cost  service_time

travelling time function f: each line represent the travelling time function between two locations in such order: (0->0,0->1,0->2,...0->n,...,n->0,n->1,...,n->n). In each line, each value represent the value of f for one time-step

f(time_step_0)  f(time_step_1)  ...   f(last_time_step)





  
