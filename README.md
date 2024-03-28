# AnisotropicDBSCAN

Here you find the google colab: https://colab.research.google.com/drive/1ka_BDGjM-p0vUBjBz-zWj2X9_bdKaGDm?usp=sharing

## Before you start 
Please run the cells "Imports", "Init Simulation functions", "Init cluster functions" before you execute any other cell. 

## Simulate a cell 
First, you need to define the simulation parameters. 
- cylinder_Radius: Radius of the cell (simulated as a cylinder) 

- cylinder_len_x: Length of the cell in x direction 

- std_true: The true standard deviation (or localization error) of each simulated localization      within a cluster. It will be applied on all three coordinates (dimensions). 

- std_x: After the true standard deviation is applied on each point this will be applied on top of that in x dimension.
  
- std_y: After the true standard deviation is applied on each point this will be applied on top of that in y dimension.

- std_z: After the true standard deviation is applied on each point this will be applied on top of that in z dimension.

- clusterCenters: Number of clusters that should be placed inside the cell.

- clusterN: Number of points per cluster that should be simulated. Points that are placed outside the cell volume (by chance after the errors are applied) are dropped out and not replaced.

- noiseN: Number of points that are uniformly distributed within the cell volume.

After all parameters are set you can run the "Demo cell simulation" to create an interactive 3D representation of the cell. All data will be accessible in the data frame "cluster_df".

## Cluster the simulated data 

First, you need to define the DBSCAN paramerters.

- min_num_points: Minimum number of points in DBSCAN

- epsilon_xy: Epsilon parameter for the xy plane.

- epsilon_z: Epsilon parameter for the z dimension (if same as xy it will be the classical isotropic DBSCAN)

Finally, you can run the "Demo anisotropic clustering" and afterward the "Show cluster result" cells to perform the clustering and visualize the result. All points in the final plot are colored by the assigned cluster lable. 
 
