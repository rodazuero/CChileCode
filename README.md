# Parents and Chidlren. A collective model of Household Behavior and Child Development
This repository includes the files necessary to replicate the results of the paper ``Parents and Chidlren. A Collective Model of Household Behavior and Child Development". The C++ code is run using (GCC) 4.4.7 compiler. The Makefile was designed for a CentOS 6.8 operating system (Linux). The following environmental variables need to be defined in the Makefile in order to run the code properly:

1. HOME. Home directory.  The directory should include the code and the csv used as input. 
2. OMP_NUM_THREADS. Number of threads used in parallel when estimating the model. Default is set to 32. It is not necessary to run threads in parallel in order to estimate the model but it certainly makes it faster. 
3. INCDIR1. Directory where the gsl library is included. If you don't have the gsl library, you can install it with admin rights. See this link: http://askubuntu.com/questions/490465/install-gnu-scientific-library-gsl-on-ubuntu-14-04-via-terminal
4. INCDIR2. Directory where the boost library is included. If you don't have a boost library, you can install it by running 
$sudo apt-get install libboost-all-dev
In a standard Ubuntu machine. 
5. INCDIR3. Directory where the the NLopt library is included. NLopt is not part of the usual "yum" or "get" installation packages. However, I have configured the necessary lines of code necessary to install it. All you need to do is run:
$make nloptinst

#Estimation results

The estimates of the model are obtained by running the C++ code in MainParallel.cpp. It uses as input the data in "BEHAVIORAL1.csv" and the generated output is "PAROPTFOUNDPARALLEL.csv". In order to replicate the estimation results you need to run
make parallelrun

#Smoothing distribution

In order to replicate the results of the smoothing distribution you need to run
make smoothdistrun




