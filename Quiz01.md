# Quizzes
## Quiz 01 - 2/4/2019 - Jill Mead ##

_**1. How can you determine the data type of a variable? (3 pts)**_ <br>

  Your answer: b.  Use the type function. <br>

_**2. What is the data type of ‘this is what kind of data’? (3 pts)**_ <br>
  
  Your answer: d. String <br>
  
_**3. Choose two built-in functions within Python that are not covered as examples in the Class02 outline.  Give a brief description of what the function does and provide an code example of how the function is called (you do not need to provide the result) (6 pts)**_ <br>

Function 1: range()
Description: Returns a sequence of numbers, given certain parameters
Code Sample: range(start, stop, step) 
```python
x = range (1, 10, 2)
for n in x
print(n)

##result
##2
##4
##6
##8
##10


```
Function 2: sorted()
Description: Returns an ascending or descending sorted list
Code Sample:<br>
```python
a = ("z", "p", "y")
x = sorted(a)
print(x)

##result ['p', 'y', 'z']



```
_**4. In Github, the place where all the code for a single project is stored is called a.. (3 pts)**_ <br>

a. Fork<br>
b. Code Store<br>
c. Repository<br>
d. Organization<br>

Your answer: c. Repository<br>

_**5. Write a script that calls the Dissolve tool (the one in the Data Management toolbox) on a county boundaries shapefile using the "STATE" attribute as the dissolve field. The resulting shapefile should be named "states.shp" and multipart features should NOT be allowed. Show your syntax for the Dissolve geoprocessing tool within the starter code below.  You may use the "counties.shp" included in the Quiz01_counties.zip to test your script. (10 pts)**_ <br>

```python
import arcpy
import os

path = r"C:\Users\jill\Dropbox\GIS Programming\County_Dissolve.gdb"
county_dissolve = arcpy.Dissolve_management(os.path.join(path,"counties.shp"), os.path.join(path,"county_bdy_dissolve.shp"), "STATE", "", "SINGLE_PART", "DISSOLVE_LINES")
```
