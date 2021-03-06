=======================================================
CMCpy -- Code-Message Coevolution Models in Python
=======================================================

CMCpy provides an object-oriented python API, together with command-line
interface executables, that implement "Code-Message Coevolution" models.
These published evolutionary models pertain to the evolution by natural
selection of a genetic code in coevolution with a population of
protein-coding genes.

Formally, CMC models are sets of quasispecies coupled together for their
fitness through a genetic code. The system alternates between quasispecies
equilibration and adaptive hill-climbing through codon assignments and
reassignment by code mutation.

CMCpy can reproduce the statistics and results of [Ardell_and_Sella_2001]_,
[Sella_and_Ardell_2002]_, [Ardell_and_Sella_2002]_ and
[Sella_and_Ardell_2006]_. CMCpy additionally implements additional
extensions that have not yet been studied in published work. It is easliy
feasible to extend the present code-base to implement the model studied by
[Vetsigian_et_al_2006]_.

CMC evolutionary trajectories are partly a sequence of eigensystem
solutions. Qualitative differences in results on different platforms can
originate from differences in convergence criteria when power method-based
eigensystem solvers are used, or from differences in floating point
representations. Python defers to the platform C library for float
representation. The default eigensystem solver is the eig() function in
Numpy.

Dependencies 
============================================ 

CMCpy relies heavily on, and absolutely requires, numpy as a prerequisite.
You should install numpy with the easy_install framework to be detected as
installed when installing this package. 

If you wish to play with an experimental CUDA-based power-method eigensystem
solver, you must install pycuda. This implementation is not faster than the
NumPy default solver for many systems.


Installation
============================================
			
This installer requires setuptools, the most recent python packaging
framework. If you do not already have this installed, this package
will install it for you, so long as you have network access. Otherwise
preinstall the correct version of setuptools using the EasyInstall
installation instructions at
http://peak.telecommunity.com/DevCenter/EasyInstall#installation-instructions 

If you need to install this package somewhere other than the main
site-packages directory, install setuptools using the instructions for
Custom Installation Locations before installing this package. The
instructions are here:
http://peak.telecommunity.com/DevCenter/EasyInstall#custom-installation-locations

If you have downloaded the source-code package, the easiest way to
install the package is to execute (from within the source root directory)::

	easy_install .

Mac users may need to run this command with "sudo" prepended.

Usage
============================================

CMCpy comes with an executable inside the bin subdirectory to the
installation source package, a UNIX-compatible script called "cmc". 

Additionally, a platform-specific executable may be automatically generated
on installation.

Published results with CMC models may be (at least qualitatively) reproduced
through the --demo option to the executables.

Also try running the --help option to the executables after installation and
for a command-line example.

Programmers may use the executable in bin as a guide and template for how to
program against the cmcpy API.
		       			  
Documentation 
============================================ 

Some documentation of the cmcpy API is available within the "doc"
subdirectory of the source distribution. HTML, pdf and texinfo alternative
formats are provided.

Licensing and Attribution 
============================================

The CMCpy project is distributed under the terms of the Apache License 2.0
as described in the file LICENSE.txt

Please cite Becich et al. (2012) in all scientific works that use this code.

Release Notes
============================================
The most recent version is 0.1 released October 2012.

See CHANGES.txt for version-related changes to the CMCpy code-base.

References
============================================

.. [Ardell_and_Sella_2001] D.H. Ardell and G. Sella (2001). On the evolution of redundancy in genetic codes. `Journal of Molecular Evolution 53(4/5):269-281`_.

.. [Ardell_and_Sella_2002] D.H. Ardell and G. Sella (2002). No accident: genetic codes freeze in error-correcting patterns of the standard genetic code. `Philosophical Transactions of the Royal Society of London B 357:1625-1642`_.

.. [Sella_and_Ardell_2002] G. Sella and D.H. Ardell (2002). The impact of message mutation on the fitness of a genetic code. `Journal of Molecular Evolution 54(5):638-651`_.

.. [Sella_and_Ardell_2006] G. Sella and D.H. Ardell (2006). The coevolution of genes and genetic codes: Crick's frozen accident revisited. `J. Mol. Evol. 63(3):297-313`_.

.. [Vetsigian_et_al_2006] Vetsigian K., Woese C. R., Goldenfeld N. (2006). Collective evolution and the genetic code. `Proc. Natl. Acad. Sci. U.S.A. 103, 10696-10701`_.


.. _Journal of Molecular Evolution 53(4/5):269-281: http://dx.doi.org/10.1007/s002390010217

.. _Philosophical Transactions of the Royal Society of London B 357:1625-1642: http://dx.doi.org/10.1098/rstb.2002.1071

.. _Journal of Molecular Evolution 54(5):638-651: http://dx.doi.org/10.1007/s00239-001-0060-7

.. _J. Mol. Evol. 63(3):297-313: http://dx.doi.org/10.1007/s00239-004-0176-7

.. _Proc. Natl. Acad. Sci. U.S.A. 103, 10696-10701: http://www.pnas.org/cgi/pmidlookup?view=long&pmid=16818880
