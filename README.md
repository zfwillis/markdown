# R Pet Assignment ~ By Fabrizio Guzzo & Billy Hyatt-Otovic 
## Exploring Vectorized Operations and Base R Pipe
#### Emails:
       fgguzzo@loyola.edu
       wjhyatt-otovic@loyola.edu


### **Goals:**
    This assignment explores two core features of the R programming language:

    1. **Vectorized operations** (element-wise calculations without explicit loops).
    2. **The native pipe operator** (`|>`) for readable, sequential data transformations.
    

### Introduction

    R’s vectorized operations allow you to perform computations on entire vectors or matrices in a single step, eliminating the need for loops. The **native pipe operator** (`|>`) chains operations together, improving code readability while using only base R functions.
    
    
### Set-Up Instructions

    There are a few ways to run R on one of the Potter-Boxes:
        1.) (Suggested) Run the handout.R as a script: `Rscript Handout.R`
        2.) Use the RStudio application available via the application menu.
        3.) Open a terminal and type `R` to start the interpreter.
        4.) (Native-download of Rstudio): https://posit.co/download/rstudio-desktop/ 

### Task 1: Vectorized Euclidean Norm (4 points)

    **Write a function `euc_norm(x)` that calculates the Euclidean norm (magnitude) of a numeric vector `x` using vectorized operations only (no loops).**

    Formula:
        Euclidean Norm = ||v|| = √(v₁² + v₂² + ... + vₙ²)
    
    Example:
        For `x = c(3, 4)`, the output should be `5 = sqrt(3^2 + 4^2)`
        
        

### Task 2: Vectorized Matrix Scaling (4 points)

    **Write a function `scale_matrix(mat)` that centers each column of a matrix by subtracting its mean, using vectorized operations only.**
    
    Example:
    ```
    mat <- matrix(1:9, nrow = 3)
    print(mat)  
    # Output (column means become 0):
    #      [,1] [,2] [,3]
    # [1,]   -1   -1   -1  
    # [2,]    0    0    0  
    # [3,]    1    1    1 
    ```


### Task 3: Piped Data Analysis (6 points)

    **Using the built-in `mtcars` dataset and the base R pipe (`|>`):**

    1.) Filter rows where `mpg > 20`.
    2.) Group the filtered data by `cyl` (number of cylinders).
    3.) Calculate the mean `hp` (horsepower) for each group.


### Task 4: Piped Data Visualization (6 points)

    **Using `mtcars` and base R pipes (`|>`):**

    1.) Filter `mpg > 15`
    2.) Create a new column `power_to_weight = hp / wt`
    3.) Group by `cyl`
    4.) Calculate the median `power_to_weight` per group
    5.) Plot the results as a bar chart using **base R graphics**

    **Required Plot Elements:**
    - Title: "Power-to-Weight Ratio by Cylinders"
    - X-axis: `cyl`
    - Y-axis: "Median Power-to-Weight"


    
### Grading
| **Criteria**                 | **Full Credit**| **Partial Credit**|  **No credit**     | **Points Earned** |  
|------------------------------|----------------|-------------------|--------------------|-------------|  
| Task 1                       | Correct vectorized implementation (no loops) | Uses partial vectorization | Uses loops/incorrect result | ?/4 |  
| Task 2                       | Correct column-wise centering via vectorization | Partial vectorization (e.g., uses apply) | Uses loops/incorrect output | ?/6 |  
| Task 3                       | Correct pipe chain with filter, group_by, summarize|Minor errors in logic/formatting | Missing key steps | ?/6 |  
| Task 4                       | Full pipeline + plot with required elements | Missing 1-2 plot elements or pipeline steps | No plot/incorrect transformations | ?/4 |  
| Use of Vectorization/Pipes   | All tasks use required R features appropriately | 1-2 misuses | Frequent violations | ?/2 | 
| Code Style                   | Clean, readable code with comments | Minor readability issues/formatting | Unreadable/spaghetti code | ?/2 |  

### Total Points **_/24**
