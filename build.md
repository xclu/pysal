# Building pysal source release

As of version 2.0 PySAL has become a meta-package that combines a family of spatial analysis packages into a single source distribution.

This document provides instructions on the preparation of the meta-package


## Building

0. Edit subtags to pin release versions for federated packages
1. `make  download`
2. edit convert.py and change `init_lines` at the bottom to have new version number
2. `make convert`
3. `make test`
4. create changelong
5. make src
6. test source release




## Files 


Makefile - build scripts

subtags - lists the release tags for each package that are part of the meta-package release

package.yml - heirarchy of pysal meta-package structure. Note that only the packages listed in `subtags` are released.

## Changelog

After building, detailed tables and reports for the changelog can be generated by running the two notebooks:

- `gitcount.ipynb`
- `gitcount_tables.ipynb`
