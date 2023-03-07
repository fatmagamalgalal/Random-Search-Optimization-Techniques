# Random-Search-Optimization-Techniques

## Genetic Algorithm

![genitics](https://user-images.githubusercontent.com/43317809/223312810-0f39a068-fdc1-4656-9044-d4c402bd8153.jpg)


### Pseudo code:

1 - Calculate the distance matrix for data points

2 - Generate the initial population
	
	In this step, you can generate a random population or use other heuristic or meta-heuristic techniques to generate it

3- Start iterating n times:

	3.1 Elite the best solutions in the current population
  
	3.2 Perform crossover with a specified probability
  
	3.3 Mutate some solutions with a specified probability
  
	3.4 Form the new population
  
  
### Crossover:

1- Choose 2 parents with a tournament selection 'best fitness from a random sample'

2- Toss a coin and perform partially mapped crossover if the probability is less than crossover probability, else pass the parents to the next generation

3- In case of partial crossover, compare the child with its parent and pass the one with the highest fitness to the next generation.


### Partially mapped crossover:

1- Generate 2 random split points

2- Swap the genes within the generated range with one condition: there are no duplicate genes in the same chromosome. for more info: 

![image](https://user-images.githubusercontent.com/43317809/223313035-9ab487d7-ed24-463e-b04a-3770306b092e.png)


### Mutation:

There are many ways to perform mutation.

The one used here is swapping 2 random genes in the given chromosome after tossing a coin



## Ant colony Algorithm


![An-illustration-of-ant-colony-optimization](https://user-images.githubusercontent.com/43317809/223312922-0498762c-47bc-427b-b172-a0f3ed3afbc6.png)



### Pseudo code:

1 - Calculate the distance matrix for data points

2 - Generate the initial population

In this step, you can generate a random population or use other heuristic or meta-heuristic techniques to generate it

3- Generate the initial pheromone matrix then update it using the initial population

3- Start iterating n times:

	3.1 Construct a new population

	3.2 Update the pheromone matrix with the new population
  

### Construction:

Construct n solution. To construct each one:

1- Choose a random point as a start

2- Calculate p value between this point and other unvisited points

3- Select the point with the max p value as the next destination

4- Add the selected point to the path 

5- Repeat until constructing the whole path

