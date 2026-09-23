# This is the [KROME](https://kromepackage.org) repository

KROME is a nice and friendly package to model chemistry and microphysics 
 for a wide range of astrophysical simulations. 
 Given a chemical network (in CSV-like format), it automatically 
 generates all the routines needed to solve the kinetics of the system, 
 modeled as a system of coupled Ordinary Differential Equations. 
 It provides various options that make it unique and highly flexible. 
 Any suggestions and comments are welcome. KROME is an open-source 
 package, GNU-licensed, and any improvements provided by 
 the users are well accepted. See disclaimer below and GNU License 
 in gpl-3.0.txt.

--------
## How to install and test KROME
The basic KROME installation is
```
git clone https://github.com/tgrassi/krome.git
```
Test with (see below on how to install gfortran)
```
cd krome
./krome -test=hello
cd build
make # if you use Ifort/Ifx
make gfortran # if you use gfortran
./test
```
You should get something like
```
Test OK!
```

To plot, you can use this Python command (or the gnuplot instruction from the output)
```
python -c "import matplotlib.pyplot as plt;import numpy as np;data = np.loadtxt('fort.66');plt.plot(data[:, 0], data[:, 1:]);plt.show()"
```


---
## Get help

To get support or receive news about KROME, please refer to our user mailing list: 

 - https://groups.google.com/forum/#!forum/kromeusers


More information on the wiki

 - https://github.com/tgrassi/krome_wiki

Additional material can be found on the Computational Astrochemistry Schools website

 - http://kromepackage.org/bootcamp/

--------
## How to install gfortran
To install gfortran on Ubuntu, type

`sudo apt-get install gfortran`

or [this on OSX](http://skipperkongen.dk/2012/04/27/how-to-install-gfortran-on-mac-os-x/) or install [gcc using brew](https://formulae.brew.sh/formula/gcc).

Note, you might need to update Xcode to the latest version before the `brew install gcc` command.

You might get a library error when compiling PROTO (`make`). This could be solved by deactivating conda (`conda deactivate`).    

---
## Authors

Written and developed by Tommaso Grassi
```
 tgrassi@mpe.mpg.de               
 MPE, Garching, Munich, Germany
```

and Stefano Bovino
```
 stefano.bovino@uniroma1.it            
 Università La Sapienza, Roma, Italy
```

Contributors: J.Boulangier, T.Frostholm, D.Galli, F.A.Gianturco, T.Haugboelle,
  A.Lupi, J.Prieto, J.Ramsey, D.R.G.Schleicher, D.Seifried, E.Simoncini,
  E.Tognelli

--
# How to cite
Refer to the original paper https://ui.adsabs.harvard.edu/abs/2014MNRAS.439.2386G
```
@ARTICLE{2014MNRAS.439.2386G,
       author = {{Grassi}, T. and {Bovino}, S. and {Schleicher}, D.~R.~G. and {Prieto}, J. and {Seifried}, D. and {Simoncini}, E. and {Gianturco}, F.~A.},
        title = "{KROME - a package to embed chemistry in astrophysical simulations}",
      journal = {\mnras},
     keywords = {astrochemistry, methods: numerical, ISM: evolution, ISM: molecules, Astrophysics - Astrophysics of Galaxies},
         year = 2014,
        month = apr,
       volume = {439},
       number = {3},
        pages = {2386-2419},
          doi = {10.1093/mnras/stu114},
archivePrefix = {arXiv},
       eprint = {1311.1070},
 primaryClass = {astro-ph.GA},
       adsurl = {https://ui.adsabs.harvard.edu/abs/2014MNRAS.439.2386G},
      adsnote = {Provided by the SAO/NASA Astrophysics Data System}
}

```

---
## Speed test

If you want to test how fast KROME is on your machine, go [here](https://bitbucket.org/tgrassi/krome_speed_test/overview).

---
## Disclaimer


KROME is provided "as it is", without any warranty. 
 The Authors assume no liability for any damages of any kind 
 (direct or indirect damages, contractual or non-contractual 
 damages, pecuniary or non-pecuniary damages), directly or 
 indirectly derived or arising from the correct or incorrect 
 usage of KROME, in any possible environment, or arising from 
 the impossibility to use, fully or partially, the software, 
 or any bug or malfunction.
 Such exclusion of liability expressly includes any damages 
 including the loss of data of any kind (including personal data)

---
## Trusted commit

Additional notes: this version of KROME is a developer version,
 while the stable version has been dropped. For this reason, we
 warmly recommend checking the status of the release by using the
 test website
 http://kromepackage.org/test/

 More information on the "tested" version here
 https://bitbucket.org/tgrassi/krome/wiki/stable_version
