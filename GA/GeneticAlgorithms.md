# Genetic Algorithms Explained By Example

- [Genetic Algorithms Explained By Example](https://www.youtube.com/watch?v=uQj5UNhCPuo)
- [Genetic Algorithm from Scratch in Python](https://www.youtube.com/watch?v=nhT56blfRpE)

---

Evolutionary Algorithms use natural solutions to approximate 'optimal' solutions for a problem.

Uses a population of possible solutions; for Knapsack, a combination of items in a backpack.

Each specimen has a genome that encodes the solution: binary encoding of the content in the backpack. `1` indicates the item is present, `0` indicates it is not.

Set of all genomes present is called the generation. Generation 0 is a random mess of solutions; evolution starts with chaos.

Fitness function evaluates how good a given solution is. Natural selection. Higher fitness scores are used to generate the next solution. Two parents, cut the genome in half at a random part and swap them; single point cross over function. 

No guarantee to not destroy current solutions. Therefore, mutation. Randomly change a bit of the genome. Loop until satisfying solution found or set number of generations.

- Genetic representation of a solution
- Function to generate new solutions
- Fitness function
- Select function to select the next generation
- Crossover function
- Mutation function

Solutions could be expressed as graphs. 

Multi-parent recombination.

Non-deterministic

---

Evolutionary Algorithms are optimisation and search heuristics inspired by natural selection.

They use a population of possible solutions and iteratively evolve them towards an optimal, or near optimal, solution.

Population of Possible Solutions
- Each candidate solution is enconded as a genome
- For the Knapsack problem, genomes could be represented as binary strings
    - A `1` indicates that the item is included
    - A `2` indicates that the item is not included
- The entire set of genomes at any given iteration is called a *generation*
- Generation 0 is usually a randomly generated set of solutions; evolution starts with disorder

Fitness Function
- Evaluates the quality of a given possible solution
- Higher fitness solutions are selected for reproduction
- Works as a natural selection mechanism; survival of the fittest

Solution Function
- Determines which specimens from the current generation will be chosen as parents to generate the next generation
    - Tournament Selection (random subset, best one wins)
    - Rank-Based Selection (sorted by fitness, best get higher probability)
    - Roulette Wheel Selection (probability based on fitness)

Crossover Function
- Combines the genomes of two (or more) parent solutions to create offspring
- Single Point Crossover
    - A random point in the genome is chosen
    - The two parents swap their parts beyond this point
- Multi Parent Recombination
    - More than two parents contribute genetic material to generate new solutions

Mutation Function
- Introduces small, random changes to genomes to maintain diversity and prevent premature convergence
- Flip a random bit in the genome
- Ensures solutions do not stagnate by escaping local optima

Evolutionary Process
- Loop through generations, apply selection, crossover and mutation until
    - An optimal or satisfactory solution is found, OR
    - A set number of generations is reached
