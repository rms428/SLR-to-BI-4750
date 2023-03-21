# Week 9 Lab - Extreme Value Analysis

This repository contains the lab notebook for Week 9 of BEE 6940, Climate Risk Analysis. 

If enrolled in the class, a PDF of the completed notebook, **with all cells evaluated**, should be submitted to Gradescope *no later* than Monday, March 27, at 1:00pm. 10% will be deducted for each day that the notebook is late.

## Prerequisites

1. [Install Julia](https://julialang.org/downloads/) before beginning this lab. This notebook was developed with version 1.8.2, but any 1.8.x should work (there could be some issues with other versions, depending on what's changed).
2. If necessary, [install git](https://happygitwithr.com/install-git.html) and [create a GitHub account](https://github.com). 
3. [Clone the repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository). I recommend doing this in a dedicated `BEE6940/` folder, which can also house homework assignment repositories and lecture notes. You can clone directly into the `BEE6940/` folder.   For Windows (or from another graphical interface), just create a `BEE6940` folder, then a `labs` folder inside of that, then clone into that folder. Or to clone into a `BEE6940/labs` folder, from a command prompt:
    ```bash
    cd BEE4750/
    mkdir labs
    cd labs/
    git clone https://github.com/ClimateRiskAnalysis/lab09.git
    ```

## Opening The Notebook

1. To interact (view and run) the notebook, there are two options:
  - Install an integrated development environment, or IDE (I recommend [VS Code](https://code.visualstudio.com/) with the [Julia extension](https://marketplace.visualstudio.com/items?itemName=julialang.language-julia)). 
  - Use the [`IJulia.jl` package](https://github.com/JuliaLang/IJulia.jl). I've included this in the project environment (discussed below), so no further steps are needed.  
2. Opening the notebook will depend on what you decided to do in the previous step. 
  - If you installed VS Code, you should be able to just open `lab05.ipynb` and everything should just work. 
  - If you're using a different IDE, Google how to make sure that it is set up to run a Julia notebook.
  - If you want to use `IJulia.jl`, open a Julia prompt. You can do this by:
    - Using the `Julia-1.8` or equivalent graphical program, type `cd("BEE6940/labs")` or whatever path points to your lab notebook folder;
    - Navigating to your `BEE6940/labs/lab05` folder and typing `julia` to open the prompt.Then:
    
      ```julia
      import Pkg
      Pkg.activate(".")
      using IJulia
      notebook()
      ```
      and you can navigate to and open `lab09.ipynb`.

## Learning Objectives

After completing this lab, students will be able to:
- fit block maxima and peaks-over-thresholds models to extremes of environmental data;
- compute and analyze posterior prediction intervals for return periods.

## Dependencies

This notebook uses the following packages:
- `DataFrames.jl`
- `DataFramesMeta.jl`
- `CSV.jl`
- `Plots.jl`
- `StatsBase.jl`
- `Optim.jl`
- `Distributions.jl`
- `StatsPlots.jl`
- `Turing.jl`
- `Dates.jl`
- `Measures.jl`