# Deployment Frequency
A GitHub Action to roughly calculate DORA deployment frequency

## Calculation: 
- Get the last 100 workflows
- For each workflow, see if it started in the last 30 days, and add it to a secondary filtered list - this is the number of deployments in the last 30 days
- With this filtered list, divide the count by the 30 days for a number of deployments per day
- Then translate to friendly n days/weeks/months. 
- Open question: what if there are multiple workflows?

## Inputs:
Workflows: required. string array of the name of the workflows to process
Org/Owner: will use environment variables
Repo: will use environment variables
Default branch: optional, defaults to main. 
Number of days (optional- defaults to 30)
