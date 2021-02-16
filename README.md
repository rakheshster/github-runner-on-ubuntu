# What is this?

[![Build Status](https://dev.azure.com/rakheshster/Azure%20Build/_apis/build/status/rakheshster.github-runner-on-ubuntu?branchName=master)](https://dev.azure.com/rakheshster/Azure%20Build/_build/latest?definitionId=2&branchName=master) [![awesome-runners](https://img.shields.io/badge/listed%20on-awesome--runners-blue.svg)](https://github.com/jonico/awesome-runners)

This is an ARM template that will create a self-hosted Linux x64 (currently Ubuntu 18.04, soon to be 20.04) GitHub runner on Azure. You don't need to register the runner against your repo. The pipeline will automatically do so. 

The pipeline takes the following inputs:
  * TOKEN - your GitHub [personal access token](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token). *Note* this is not the token of the self-hosted runner. 
  * REPO - the `username/repo` of the GitHub repo you wish to register the runner against (e.g. `rakheshter/kea-knot`)
  * RUNNER_VER - the version of the runner to download and install 
  * RESOURCEGROUP - the name of the resource group to use in Azure (put whatever name you wish to use - doesn't matter)
  * AZ_CONNECTION - the name of your service connection to Azure
