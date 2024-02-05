# Polarizing_Nanocomp_Project
 Scripts for polarization of nanocomposite materials project. Initial scripts written by David Hally, Updated by Brett Henderson and Archita Adluri.




How To Run:


To Check During Calculation:

Steps 4-6 MUST before continuing to 7-9, increase number of steps otherwise. These scripts assume that the material is an insulator and will most likely fail otherwise. If using QuantumEspresso Versions newer thqn 6.0, some of the flags/inputs may have changed. Check https://www.quantum-espresso.org/Doc/INPUT_CP.html

Restarting: change restart flag from reset_counters to restart. CHnage ndr flag to current binary (i.e restarting step 6 would have ndr=56)



Parts of the scripts:

Section : ATOMIC_POSITIONS (angstroms)

Include the .xyz coordinates in angstroms -- no spaces before the coordinates.

Section: ATOMIC_SPECIES

Include atomic species label, atomic number and corresponding pseudopotential file name. The pseudopotentials must be copied in the same directory as the .in files. Make sure there are no spaces

Example:
ATOMIC_SPECIES
 O  16.00 O.pz-n-rrkjus_psl.0.1.UPF
 Ag 107.9 Ag.pz-d-rrkjus.UPF
 Mg 24.305 Mg.pz-bhs.UPF

Section: CELL_PARAMETERS (angstroms)

Matrix of cell parameters in angstrom. Can obtain from Avogadro or other model-building code.
