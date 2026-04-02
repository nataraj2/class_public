# How to run ``class``?

The class code generates the transfer function (or the spectrum) for the overdensity that is then used by the [CosmicIC](https://github.com/cosmo-suite/NyxCompilationAndRunning/tree/main/CosmicIC) codebase to generate the initial condition for the particle locations which can then be used in Nyx.  

To run the code
1. `git clone https://github.com/nataraj2/class_public.git`
2. `cd class_public`
3. `make -j8`
4. `cp ForNyx/<.ini file>`
5. `./class <.ini file>`
6. The output will be written in the `output` directory. The output files start with the same string as the `.ini` filename. The file of interest is `*00_tk.dat` file. That has the same structure as the cmb.tf` file that exists in the [CosmicIC](https://github.com/cosmo-suite/NyxCompilationAndRunning/tree/main/CosmicIC) codebase.
7. Python scripts to do the plotting and comparing is in ???.

# The inputs
There are two `.ini` files in the `ForNyx` directory.  
1. ```inputs_to_reproduce_cosmicic_result.ini``` - this inputs file contains the same cosmological parameters as the `inputs.par` file in [CosmicIC](https://github.com/cosmo-suite/NyxCompilationAndRunning/tree/main/CosmicIC) has. So, it gives the same result as the `cmb.tf` file in [CosmicIC](https://github.com/cosmo-suite/NyxCompilationAndRunning/tree/main/CosmicIC) codebase. So, the ```output/inputs_to_reproduce_cosmicic_result00_tk.dat``` and `cmb.tf` will give good quantitative agreement on comparison with the python script ???  
2. ```inputs_4096_80Mpcbyh_Jacobus_etal.ini``` - this inputs file contains the same cosmology as [Jacobus et.al](https://iopscience.iop.org/article/10.3847/1538-4357/acfcb5/meta)
