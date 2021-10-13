# Rectangular Hydraulic Fractures
The objective of this code is to create features that mimic hydraulic fractures

Tools needed for the analysis
```python
from mpl_toolkits.mplot3d import Axes3D
from mpl_toolkits.mplot3d.art3d import Poly3DCollection
import matplotlib.pyplot as plt
```
Define corner points of rectangles
```pyhon
frac1 = [(7,6,10),
         (7, 6, 20),
         (13, 6, 20),
         (13, 6, 10)]

frac2 = [(2,9,13),
         (2, 9, 17),
         (18, 9, 17),
         (18, 9, 13)]

frac3 = [(7,12,10),
         (7, 12, 20),
         (13, 12, 20),
         (13, 12, 10)]

fractures = [frac1, frac2, frac3]
```

Define figure and plot point sets
```python
fig = plt.figure()
ax = Axes3D(fig)

facets = Poly3DCollection(fractures)
facets.set_facecolor(['blue', 'green', 'red'])
ax.add_collection3d(facets)
ax.set_xlabel('x')
ax.set_ylabel('y')
ax.set_zlabel('z')
```
Define view range
```python
ax.set_zlim3d(0, 20)                    
ax.set_ylim3d(0, 20)                    
ax.set_xlim3d(0, 20)
```
&nbsp; 


![alt text](https://github.com/MouinAlmasoodi/3D_Fractures/blob/main/3DFracs.JPG)
