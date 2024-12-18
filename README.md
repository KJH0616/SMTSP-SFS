# SMTSP-SFS Dataset

This repository provides benchmark datasets used in the study "Minimizing Total Tardiness for the Single Machine Scheduling Problem with Sequence-Dependent Family Setup Times via Deep Reinforcement Learning." These datasets are specifically designed to evaluate algorithms for solving single machine scheduling problems while minimizing total tardiness, considering sequence-dependent family setup times.

## Repository Structure
### Dataset Directory
The datasets are categorized based on due date conditions:
  * Loose Due date
  * Tight Due date

### Subdirectories
Each dataset directory under each due date condition contains subdirectories named based on the number of jobs and families in each dataset:
  * Example: J100_F13 indicates instances with 100 jobs and 13 families
  * Each subdirectory contains 10 problem instances
  
## Problem Instance Description
Each problem instance includes the following attributes:
 * Problem Instance: Identifier for the specific dataset
 * Number of jobs: Number of jobs in the instance
 * Number of families: Number of job families
 * Tau (τ): A parameter related to the due date tightness
 * R: A parameter controlling the due date range
 * Processing times: An array of processing times for each job
 * Due dates: An array of due dates for each job
 * Setup times: A matrix of setup times between jobs belonging to different families
 * Families: An array indicating the family to which each job belongs

### Example File Details
* Processing times: Time taken to complete each job.
  For example, [55, 120, 481, 100, 416, 403, 135, 55, 70, 160] represents 10 jobs with varying processing times.
* Due dates: The deadlines for each job.
  For example, [829, 1317, 1300, 995, 1345, 533, 728, 1084, 1104, 1136] represents the due dates for the 10 jobs.
* Setup times: A 2D array representing the setup times between jobs from different families.
  For example, [[0, 61], [60, 0]] indicates different setup times between two families.
* Families: The family to which each job belongs.
  For example, [1, 1, 0, 1, 0, 0, 1, 1, 1, 1] shows that 10 jobs belong to two different families (0 or 1).

# Usage Instructions
Use these instance files to evaluate the performance of various scheduling algorithms.
Design scheduling algorithms that minimize tardiness by considering job due dates and family-dependent setup times.
