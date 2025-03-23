# comp_research_takehome

The purpose of this project was to demonstrate my ability to set up a Python environment, load, inspect, and transform geospatial data, perform spatial operations, and formulate and solve a small optimization problem.

I had a data set of 100 polygons coming from a shape file, where each polygon includes a parcel_id (integer), a carbon_store attribute (floating point), and a cost attribute (floating point). I inspected the data, reprojected the data to a new coordinate system (from EPSG:4326 to EPSG:3347), and computed an adjacency matrix. The final task was to set up and solve an optimization project, where I wanted to select a subset of polygons from my file and maximize the total carbon_store attribute subject to two constraints. These constraint were: the total cost of the polygons must not exceed 50% of the sum of the cost of all the polygons, and no two polygons that share an edge must both be selected.

I did this project on a Macbook and used Anaconda and Jupyter Notebook.

My setup was as follows:
* Create a Python environment using Anaconda
  *   Download Anaconda Navigator and follow the instructions (you can search this on the web)
  *   Launch Anaconda
  *   Click on the 'Environment' tab on the left-hand side
  *   To create a new environment, press the 'create' button
  *   Name your new environment (I named mine env_take_home_comp_research)
 
* Install necessary Jupyter Notebook packages
  * Click on drop-down menu at the top in your environment in Anaconda and click 'not installed'
  * Search for 'jupyter' in the search bar
  * There will be multiple packages listed, I only needed to install the one titled 'jupyter'
 
* Install other packages
  * Follow similar steps above to install the geopandas package
  * In your new conda environment, you will also need to install Pyomo
     * Execute the command: conda install -c conda-forge pyomo
   * For setting up the optimization problem with Pyomo, I used the GLPK solver
     * Execute the command: conda install -c conda-forge glpk
    
  * Creating your Jupyter Notebook
    * You can activate your conda environment using the command: conda activate environment_name in the terminal
    * Launch Jupyter Notebook using the command: jupyter notebook
    * Create your Jupyter Notebook file
    * Import the packages geopandas, shapely, and pyomo


