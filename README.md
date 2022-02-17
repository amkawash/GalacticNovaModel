# GalacticNovaModel
iPython notebooks to build a Galactic Model of classical novae (can be edited for other transients).

Prerequisites: 1. Anaconda distribution of python.
2. mwudst, follow installation instructions here: https://github.com/jobovy/mwdust

Milky_Way_StellarDensity.ipynb has functions for a Galactic thin disk, thick disk, 2 component bulge, and halo. 
The analytic solutions for these are from Robin et al. 2003 and Simion et al. 2017. The functions defining the
various components are at the top followed by a cell that lets you set the resolution of the grid and boundary
conditions. The next cells calculate the stellar density, the total mass of each componenet and saves the Galactic 
stellar density in an array called rho_n. The last cell just plots the results.

make_nova_model.ipynb probabilistically distributes N novae based on the stellar density model made above.
You need to enter the path to the stellar density array in the second cell. There are cells to save the positions 
to a table, and plot the results. Then you can calculate the extinction using mwdust model in whatever filter you
prefer. You can then calculate the peak apparent magnitude of the transient given the distance, absolute mag, and
extinction. 



