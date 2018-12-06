# README

#### Authors: Saskia Comess & Chengcheng Qiu

#### Project title: Spatio-Temporal Data Visualization of Individual-Level Environmental Exposures

#### Introduction
### Objective
The objective of this project was to create a tool to visualize the data obtained from personal exposure monitors. Personal exposure
monitors are an increasingly popular tool for collecting individual level exposure data. However, these data are collected in large
quantity and vary by location and time. Thus, being able to easily visualize a subject's data- including spatio-temporal variation-
is a key step in ultimately being able to interpret and use the data for research.

### Approach to spatio-temporal data visualization
An essential feature of the spatio-temporal visualizer is seeing how a given exposure changes as a function of space and time. Here,
we plot three things as a function of time: geographic movement, noise exposure, and temperature exposure. Our approach could easily
be modified to plot other exposures based on the available data.

#### Install (Requirements)
This project was implemented in a Jupyter Lab file. Follow these steps in the terminal window of your computer to use the provided
Jupyter Lab file:
Download/install homebrew (brew.sh/)
Install python3 with homebrew: $ brew install python3
Install pipenv, for package management: $ brew install pipenv
Install Jupyter Lab: $ pipenv install jupyterlab
Navigate to the appropriate directory where the Jupyter Lab file that we provided is stored. To launch Jupyter Lab: $ jupyter lab

To implement this project, the following packages are required:
-os
-folium
-csv
-pandas
-numpy
-matplotlib
-datetime
-time
-ffmpeg

We installed these packages using homebrew, via the terminal window (for example: “brew install package_name” or “pipenv install package_name”)
and stored everything locally on the computer.

#### Animated plotting of geographic movement by time
To plot geographic movement by time, a csv file containing the following columns is needed: timestamp, lat (latitude), lng (longitude).
For example purposes, we have provided “user0_loc.csv.” This file must be saved in the same directory as the Jupyter notebook.
Running the animation code in the Jupyter Lab file produces an interactive map (saved as “track_loc.html”) which plots movement by time.

#### Animated plotting of exposure by time
A csv file containing information on timestamps and measurement of exposures like noise or temperature would be required to plot the
changes of exposure over time. We have provided “expo_sample.csv”, placed in the same directory as the Jupyter notebook, to demonstrate
how to produce animated plot of exposure against time. The output would be in mp4 format for each exposure measures, with datetime on
the x-axis and exposure levels on the y-axis. The example output for exposure to noise and temperature are called “sample_noise.mp4”
and “sample_temperature.mp4”, respectively, and would be used later for displaying these with the animated plotting of geographic
movement by time concurrently on the same page.


#### Viewing Movement and Exposure Simultaneously
To visualize the simultaneous spatio-temporal relationship between movement and exposure, right click on “main.html”, which has been
modified from the “track_loc.html” file that produces an interactive map and integrated with outputs of the exposure plots, and then
select “open in new browser tab”. This should display a webpage in which the animated map and exposure plots play simultaneously.


