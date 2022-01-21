# Github-Environment-Cleaner
Quick tool for cleaning up the "Environments" tab on a Github repository

## Problem
I noticed that many developers do not know how to remove inactive environments in GitHub account. For example, when you are using automatic deployment from two separate Github branches (one for staging, one for production), it create a tab "Environments" on the repository, in which both Heroku environments were shown - exactly as intended. Unfortunately, it happens that after some time one of the environments will no longer be needed. The Environments tab on my Github repo has no way to remove the environment that I no longer use. I can't seem to find any place on Github or Heroku to make Github "forget" this deployment environment.

## Solution
I have prepared a simple script that solves this problem. Before using it, you should disconnect GitHub and Heroku before doing this.

First, go to your GitHub account settings, then developer settings, then personal access tokens. Create a new token that has repo_deployments allowed. After it's generated, save the hexadecimal token, you'll need it for the upcoming API requests.

Having the token, the name of the organization and the name of the repository, you can run my script.
