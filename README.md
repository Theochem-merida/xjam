This program identifies and generates stacking sequences of high-symmetric honeycomb lattice layered materials via the Joining and Arrangement of Multilayers (JAM) notation by mapping a string of characters to the structure of a polytype using only its chemical symbols.


Installing JAM
===============

You can install and uninstall with:

```
# install
pip3 install xjam

# invoque as:
x.jam

# uninstall
pip3 uninstall xjam
```

or

```
# install
git clone https://github.com/Theochem-merida/xjam.git
cd xjam
python3 setup.py install --record files.txt

# invoque as:
x.jam

# uninstall
xargs rm -rf < files.txt
```

The JAM.inp file
===============

The user must create a JAM.inp file to control the options when running the JAM algorithm.
The JAM.inp file includes the following variables:

```
-option: INT, type of material (PL, BPL, BU, BBU)
-num_layers: INT, number of layers to stack
-poscargen: BOOL, indicates whether POSCARs are generated
-atom_list: CHAR, list of the chemical symbols of the elements in the material
-latticep: FLOAT, the lattice constant used to scale all lattice vectors
-z_vacuum: FLOAT, the vacuum space
-buckling: FLOAT, the distortion out of the plane
-distance: FLOAT, the interlayer distance
```

Running JAM
===============
```
x.jam
```

Output Files
===============
```
-JAM.out: The log file includes the computation time for each operation for the n-layer system
-jamstrings00n.txt: The generic JAM strings for the n-layer system
-sjamstrings00n.txt: The specific JAM strings for the n-layer system
-POSCAR files
```

Notes
===============
```
The program will generate the sjamstring and jamstrings of the multilayers with num_layers = 2 up to the number specified in JAM.inp
```
