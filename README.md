Protein-in-water Dataset for NMRDfromMD
=======================================

<a href="webp">
  <img src="snapshot/snapshot.png" align="right" width="25%"/>
</a>

GROMACS input files and raw trajectory files used to generate the data
and figure from [nmrdfrommd](https://nmrdfrommd.github.io). The system
consists of a protein (HEWL) in water.

## Repository structure

- **[inputs](inputs)**: Contains the LAMMPS input files.
- **[data](data)**: Contains simulation output files (``.data`` and ``.lammpstrj``)
  for various temperatures, generated from the input files. Due to their
  large size, ``.xtc`` files are not hosted in this repository. You can regenerate
  them by relaunching the simulation with LAMMPS.
- **[analysis](analysis)**: Contains Python scripts for running NMRDfromMD
  and extract NMR relaxation rates.
- **[snapshot](snapshot)**: Contains ``.png`` images of the system generated
  using VMD.

## Clone the repository

To clone the repository, run:

```bash
git clone https://github.com/NMRDfromMD/dataset-protein-in-water.git
```

To regenerate the trajectory files, navigate to the [data](data) folder:
```bash
cd dataset-protein-in-water/data
```
Update the path to GROMACS in ``run-all.sh`` to reflect your system
configuration:
```bash
gmx=
```
Then, execute ``run-all.sh``.

## License

This repository is licensed under the Creative Commons Attribution 4.0
International (**CC BY 4.0**) [License](LICENSE).
