Example MATLAB main script: “ZZvsModel.m”

The link below contains the basic steps of running MATLAB on the CHTC.
https://chtc.cs.wisc.edu/matlab-jobs.shtml

There are two parts to running MATLAB on the CHTC:
Compilation
Submission

The compilation step is described in the link above. Refer to a

Convert all script files into function files:

[rmsd_fiber,rmsd_TC,rmsd_DP,rmsd_Tout,rmsd_qdot,Re_C,Re_H] = ZZvsModel(j_C,f_D)


Convert all necessary Toolboxes into a folder of functions along with secondary functions.

Built-in MATLAB toolboxes are generally not an issue

The goal is to have a ‘functions’ folder that contains every function that the main script calls.

The structure of this folder doesn’t matter. The CHTC will recursively search over subfolders and compile all the functions it finds in the compiling step.


Prepare a csv or txt file with all the input combinations.

In this case, the csv file might look like:
0.1, 0.3
0.2, 0.3
0.1, 0.4
0.2, 0.4

Header information not needed. Make sure the order of inputs in a row matches the order of the function call (not necessary but makes things more simple)

Convert input variables to from str type to num type with str2num since all inputs from the csv file comes in str




Plotting
Still not sure how to get around this
Generally avoid functions with a plotting format for now


Outputs

Outputs can be stored in a .mat file (from the main script) but this must be executed from the MATLAB side of things.

Outputs also appear in a txt file from the CHTC, but the format is often quite messy

Use a python script or module to clean and save the data to a csv

Omit semicolons in final MATLAB



Data Pts
