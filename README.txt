There files in this directory contain the numerical results from the computational experiments discussed in the paper:

"A multicommodity flow model for rerouting and retiming trains in real-time to reduce reactionary delay in complex station areas"
Reynolds, E., Ehrgott, M., Maher, S. J., Patman, A., Wang, J.Y.T
(submitted as of 2020)

Each file contains one row for every instance, named dat_000, ... , dat_309 (there are 310 instances).
The results in each file were generated using different settings (time limit in seconds given inside the brackets):

report_basic.csv - standard column generation (600s)
report_partial.csv - standard column generation with partial pricing (600s)
report_varfix.csv - standard column generation with reduced cost variable fixing (600s)
report_varfixpartial.csv - standard column generation with partial pricing and reduced cost variable fixing (600s)
report_varfixpartialtwenty.csv - standard column generation with partial pricing and reduced cost variable fixing (20s)

The columns are the same accross all files:

SCIP Status_SCIP Status - the solve status (see SCIP documentation). N.B. The gap limit was 0.01%, and this is considered an optimal solution, in line with many commercial solvers.
Total Time_solving - Total time to read and solve the problem, or the time limit, whichever is smaller.
B&B Tree_nodes - Number of branch-and-bound nodes created during the solve process
Solution_Primal Bound - Best primal bound found during the solve process
Solution_Dual Bound - Best dual bound found during the solve process
Solution_Gap - Percentage gap between the previous two columns
Pricers_railspp_ExecTime - Total time spent executing the pricer during the solve process
Pricers_railspp_Vars - Number of variables (columns) generated in total during the solve process
Constraints_linear_MaxNumber - The number of constraints in the model (1 higher than the number of linear constraints, for implementation reasons)
cc - Number of 'OO' conflicts in the instance
cd - Number of 'OB' conflicts in the instance
dc - Number of 'BO' conflicts in the instance
journey_c - Number of train pair conflicts in the instance

Contact me on Github or by email if more information is required.
