# Introduction to Molecular Dynamics Simulation - Part 2


## Background

In the last lab, we used [OpenMM](https://openmm.org/) to perform a simple molecular dynamics simulation of alkanes in vacuum and of a water box. 
For analysis, we utilized a Python library called [MDAnalysis](https://www.mdanalysis.org/). 
Both of these software packages are open-source and offer a Python API. 
For this week's lab, we will be venturing into a different software ecosystem.

This week, you will be simulating a DNA duplex molecule under various solvation conditions using the AmberTools suite. 
Amber is a molecular dynamics software package first developed in the mid-1970s that still boasts an active developer community today. 
In fact, Dr. Nash attended the 2023 Amber Developer's Meeting (picture below)!

![Amber Developer's Meeting 2023](images/tampa2023.jpg)


While OpenMM is both free and open-source, the full Amber suite has licensing restrictions. For non-academic users, there are associated costs. However, starting in 2023, Amber became completely free for academic users, although registration and obtaining a license are still necessary.
AmberTools, a subset of Amber, is a set of software that's free for all users. 
Within this suite, there's a molecular dynamics software called `sander`.
While `sander` and other tools within AmberTools are free of charge, they are not necessarily "open source" in the same way that software like OpenMM is. 
Instead, they can be better described as 'source-available'.
If you obtain access to the full Amber program (in contrast to just AmberTools), you will find that the molecular dynamics software included is much faster and more performant than the free version.

For our lab, we will primarily be using `sander` and the associated tools in the AmberTools suite. 
In this lab, you will start at the very beginning – system preparation (this was done for you last time!). 
System preparation describes finding or making your starting coordinates, applying forcefield parameters, and writing system input files.

As you work through the lab, think about the interfaces of Amber and OpenMM. 
Amber operates using input files with the required parameters, whereas with OpenMM, you incorporated libraries and objects in a Python script.
Amber uses a much more "procedural" interface for many of its tools, while OpenMM heavily relies on an object oriented paradigm.
Amber also uses a variety of different types of tools - all mostly  executed from the terminal.
While you complete the lab, take some time to think about the differences between these two approaches to software.
Do you prefer one over the other? 
What are the advantages and disadvantages of each?

## Lab Material

To complete the lab, create an environment using the provided `environment.yaml` file.
This will create an environment called `chem274A_lab3`.

```
conda env create -f environment.yaml
conda activate chem274A_lab3
```

You can then complete the lab by [following the tutorial](https://janash.github.io/amber-dna-tutorial/).

Note that this is a tutorial that Dr. Nash is currently rewriting and updated for 2023. 
Only the tutorial through implicit solvent simulation is finished, so you will not yet be able to do the explicit solvent simulation.


