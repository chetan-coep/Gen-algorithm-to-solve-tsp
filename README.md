# Travelling Salesman Problem Solver using Genetic Algorithm in C

This project provides a solution to the Travelling Salesman Problem (TSP) using a Genetic Algorithm. The aim is to find the shortest possible route that visits each city exactly once and returns to the starting city. The implementation is done entirely in the C programming language.

## Features

- Random city generation with intelligent naming
- Option to load cities from a CSV file
- Customizable genetic algorithm parameters including population size, mutation rate, crossover rate, and number of generations
- Command-line interface for parameter configuration
- Menu-driven interactive interface for city and database selection
- Visualization of the best route using SVG graphics

## Technologies Used

- Language: C
- Standard Libraries: stdio.h, stdlib.h, math.h, time.h
- Algorithms: Genetic Algorithm including selection, mutation, and crossover
- Concepts: Euclidean Distance, fitness evaluation, randomization

## Compilation and Execution

### Prerequisites

A C compiler such as GCC must be installed on the system.

### Compilation Command

```
gcc -Wall -o result programMain.c tspSolver.c -lm
```

### Execution Command

```
./result
```

## Command-Line Options

- -c [value]: Set the maximum number of cities (default is 100)
- -p [value]: Set the population size (default is 500)
- -g [value]: Set the number of generations (default is 5000)
- -m [value]: Set the mutation rate (default is 0.08)
- -x [value]: Set the crossover rate (default is 0.85)
- -h: Display the help menu

## City Database Options

### Random Generation

Generates between 10 and 40 cities with randomized coordinates and names based on predefined prefixes and suffixes.

### CSV File Input

Accepts city data in the following format:

```
ID,CityName,X,Y
0,New York,40.7128,-74.0060
1,Tokyo,35.6895,139.6917
...
```

## Sample Output

```
Best Route Found:
Total Distance: 10345.67
Route: New York (0) -> Tokyo (1) -> Sydney (2) -> New York (0)
Time taken: 12.34 seconds
```

## Visualization

After execution, the best route is saved as an SVG file named best_route.svg. This file includes all cities, their labels, and the optimal path drawn based on their coordinates. The start and end city is visually highlighted.

## Key Functions

- genetic_algorithm: Main genetic algorithm loop
- initialize_population: Initial population of routes
- crossover: Combine two parent routes to create a child
- mutate: Apply mutation to enhance diversity
- calculate_route_fitness: Evaluate route distance and fitness
- save_route_visualization: Generate SVG representation of the best path

## Future Enhancements

- Parallelization to improve execution time
- GUI interface for city selection and visualization
- Improved scaling for visualization of larger datasets
- Input and output enhancements for better flexibility

## License

This project is open-source and free to use for educational and research purposes.

## Repository

GitHub: https://github.com/chetan-coep/Gen-algorithm-to-solve-tsp

## Author

Chetan Kamble  
Second-year Computer Science Engineering student  
COEP Technological University (formerly College of Engineering, Pune)
