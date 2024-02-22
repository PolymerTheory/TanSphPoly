# TanSphPoly

This directory contains the computer code used for off-lattice simulations of a tangent sphere model for a blend of stiff and flexible polymers. See [this paper](doi.org/10.1021/acs.macromol.1c02400) for details. 

If you use this code, please cite this github repository and the above paper.

# Code details
"offlat.cc" is the main program. The current version performs a short simulation 
from a random configuration that takes a few minutes. The parameters of the 
simulation are included among the global variables at the beginning of the 
program. To change them, you need to edit the program and recompile (the program 
is very basic). The program can start from a random configuration or read in a 
previous one from the file "positions". The program periodically records the 
configurations in the subdirectory called "dumps", writes the distribution of 
monomer centers to a file called "rho_ave", records the average radius of 
gyration and end-to-end lengths in a file called "poly_size", and writes the 
average bending energy of the stiff polymers to a file called "bend_energy".

"random.h" is a header file for the random number generator that must be present
when "offlat.cc" is compiled.

"rho_to_phi.cc" is utility that converts the distribution of monomer centers in 
the file "rho_ave" to volume fractions, which are written to the file "phi_ave".

#Use cases
Russell K. W. Spencer and Mark W. Matsen (2022) Universality of Entropic Surface Segregation from Athermal Polymer Blends Due to Conformational Asymmetry. Macromolecules 55, 4, 1120–1126

If you use this code, I would be happy to advertise your paper as a use case.

#License
This project is licensed under the MIT License - see the LICENSE.txt file for details.

