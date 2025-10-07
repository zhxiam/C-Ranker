@ Deployment

For running CRanker in Linux, you first need to install the "Matlab Compiler Runtime" environment (MCR). 

* Matlab Compiler Runtime Installation
 ** Locate the file "MCRInstaller.bin" which is situed in the MATLAB Compiler Toolbox directory.
 ** Execute it. During the installation, it will be asked you to choose a target directory. In the following, we will call it ${MCR_ROOT}.


@ Execution

Go in the C-Ranker directory, Run the ".sh" files by typing

  ./run_<app>.sh  ${MCR_ROOT}/<vXXX> <args>

where :
<app> is the name of C-Ranker commands
<args> are the usual command line arguments
<vXXX> is the version of the compiler runtime to use

* Example. 
(1) Launch the cranker_read command to read data from demo data file: testData.txt by typing
  
  ./run_cranker_read.sh  ${MCR_ROOT}/v713/  testData.txt testData.mat

The PSM records are saved in the testData.mat file.

(2) run cranker_solve read to calculate the score of each PSM record by typing

  ./run_cranker_solve.sh  ${MCR_ROOT}/v713/  testData.mat testData_score.mat

The calculated scores are saved in testData_score.mat file.

(3) put out the identified reliable PSMs by typing

  ./run_cranker_write.sh  ${MCR_ROOT}/v713/  testData.txt testData.mat


Enjoy!