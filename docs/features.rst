Features
========

Supported molecules
-------------------

List of species implemented in RADIS:

- Equilibrium: :py:data:`~radis.io.MOLECULES_LIST_EQUILIBRIUM`
- Nonequilibrium: :py:data:`~radis.io.MOLECULES_LIST_NONEQUILIBRIUM` 


Line databases
--------------

Various line database formats are supported by RADIS, and can be easily switched
to be compared. See the list of supported line databases formats: 
:py:data:`~radis.lbl.loader.KNOWN_DBFORMAT`
and refer to the :ref:`Configuration file <label_lbl_config_file>` on how to use them. 

See the comparison of two CO2 spectra calculated with [HITEMP-2010]_ and [CDSD-4000]_ 
below:

.. image:: spectrum/cdsd4000_vs_hitemp_3409K.*
    :alt: https://radis.readthedocs.io/en/latest/_images/cdsd4000_vs_hitemp_3409K.svg


Performance
-----------

RADIS is very optimized, making use of C-compiled libraries (NumPy, Numba) for computationally intensive steps, 
and data analysis libraries (Pandas) to handle lines databases efficiently. 
Line databases are automatically cached under HDF5 format. 
Extra performance improvement such as an automatic **pseudo-continuum calculation**
which improves calculation times by orders of magnitude for polyatomic molecules. 
See :ref:`Performance <label_lbl_performance>`


Compare spectra
---------------

RADIS allows you to manipulate calculated and imported spectra directly 
from the Python environment. See :ref:`Compare two Spectra <label_spectrum_howto_compare>` 


Precompute spectra
------------------

In RADIS, the same code can be used to retrieve precomputed spectra if they exist, 
or calculate them and store them if they don't. See :ref:`Precompute Spectra <label_lbl_precompute_spectra>`
