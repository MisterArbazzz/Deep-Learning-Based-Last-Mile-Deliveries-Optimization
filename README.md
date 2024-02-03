# Deep Learning Based Last Mile Deliveries Optimization

This repo exemplifies the response to the Amazon Last Mile Routing Research Challenge, which strives to incorporate actual Amazon driver experience into the best possible route planning system. The answer may be used as an Amazon SageMaker Processing Job and is based on our paper, Learning from Drivers to Address the Amazon Last Mile Routing Research Challenge. Two sample sequences produced from the same Amazon route carrying 100 parcels are displayed in the diagram below. Our approach computed the sequence on the left (driver-friendly), whereas a traditional Traveling Salesperson Problem (TSP) solver produced the sequence on the right (cost-optimal).

# Methodology

To provide user-friendly routes for last mile planning, our method hierarchically incorporates Markov model training, online policy search (i.e. Rollout), and commercial TSP solvers. The underlying TSP solver can be chosen in any way. This repository achieves a nearly equal score of 0.0372 by using OR-tools for easier integration. These outcomes are equivalent to what the top three teams on the public leaderboard have accomplished. More significantly, our approach is entirely data- and learning-driven. The PPM model can be trained using 6,000 route sequences in 4 to 5 seconds on a single CPU instance because to the lightweight and quick training method. since it does not need any custom heuristics.

Refer to lastmile_usage_directions.txt for implementation
