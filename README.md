Reinforcement Learning for Automatic Selenium Tests Prioritization and Selection in Continuous Integration

## Abstract

> Testing in Continuous Integration (CI) involves Selenium Tests prioritization, selection, and execution at each cycle.
> Selecting the most promising Selenium Tests to detect bugs is hard if there are uncertainties on the impact of committed code changes and traceability links between code and tests are not available.
> Approach for automatically learning Selenium Tests selection and prioritization in CI with the goal to minimize round-trip-times between code commits and developer feedback on failed Selenium Test.
> Learning to select and prioritize Selenium Test according to their duration, previous last execution and failure history.
> In a constantly changing environment, where new Selenium Tests are created and obsolete Selenium Test are deleted, this approach learns to prioritize error-prone Selenium Test higher under guidance of a reward function and by observing previous CI cycles.

# Configuration


`resel.py` is the main file of the project.
It provides command line arguments to control the execution.
Run `./resel.py -h` for an overview of all arguments and a description.

## Experiments

Common configuration is located in `run_experiment_common.py`, but can be overwritten from each experiment file.

- `USE_LATEX`: If True, figures are plotted by xelatex (has to be installed separately), else the standard matplotlib backend is used (default: False)
- `DATA_DIR`: Directory to store raw results of experiments (default: RESULTS)
- `FIGURE_DIR`: Directory to store exported figures from evaluation (default: RESULTS)
- `ITERATIONS`: Number of times the experiment is repeated (default: 30)
- `PARALLEL`: Run iterations in parallel (default: True)
- `PARALLEL_POOL_SIZE`: Number of parallel executions (default: 6)

