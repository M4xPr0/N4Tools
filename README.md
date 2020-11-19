<h2 align="center">N4Tools</h2>

<p align="center">
    <img src="https://img.shields.io/cocoapods/l/Cocoapods">
    <img src="https://img.shields.io/badge/python-3.7|3.8-red.svg">
    <img src="https://img.shields.io/pypi/v/N4Tools?label=N4Tools">
    <img src="https://img.shields.io/pypi/v/python-bidi?color=darkgreen&label=python-bidi">
    <img src="https://img.shields.io/pypi/v/pyfiglet?color=darkgreen&label=pyfiglet">
    <img src="https://img.shields.io/pypi/v/arabic_reshaper?color=darkgreen&label=arabic_reshaper">
    <a href="https://pepy.tech/project/n4tools"><img alt="Build Status" src="https://pepy.tech/badge/n4tools"></a>
</p>

##### What is N4Tools?
It is a library that contains a set of ready-made codes that enable you to create the most wonderful designs on the terminal.

##### N4Tools API
 - [Color](https://github.com/No-Name-404/N4Tools#Color)
 - [Text](https://github.com/No-Name-404/N4Tools#Text)
 - [Square](https://github.com/No-Name-404/N4Tools#Square)
 - [Animation](https://github.com/No-Name-404/N4Tools#Animation)
 - [ThreadAnimation](https://github.com/No-Name-404/N4Tools#ThreadAnimation)

#### Color
It is a class that allows you to colorize text professionally on the terminal.
Texts can be colored in two ways.
first way by just adding the color to the text and second ways by using reader function.

```python
from N4Tools.Design import Color
CO = Color()

# first
print ('My '+CO.RED+'red'+' and '+CO.GREEN+'green'+' text')

# second
print(CO.reader('My [$RED]red[$/] and [$GREEN]green[$/] text'))
```
All color.
```python
from N4Tools.Design import Color
from pprint import pprint

CO = Color()
pprint (CO.colors)

for color in CO.colors.keys():
    print (CO.reader(f'[${color}]{color}'))
```
Delete colors from text.
```python
from N4Tools.Design import Color
CO = Color()

text = '[$BLUE]My text Color[$/]'
text = CO.reader(text)
print(text)

text = CO.del_colors(text)
print(text)
```
All colors rgb that N4Tools support.
```python
from N4Tools.Design import Color
CO = Color()

CO.show_all_rgb_colors()
```
Create my rgb color.
```python
from N4Tools.Design import Color
CO = Color()

text = CO.rgb(203,type='FG')+'MyText'
print(text)

text = CO.rgb(203,type='BG')+'MyText'
print(text)
```
How to add rgb colors to reader function?
```python
from N4Tools.Design import Color
CO = Color()

# my rgb color
MyColor = CO.rgb(203,type='FG')

# add to Color class
CO.colors['ColorName'] = MyColor

# test:
print (CO.ColorName+'My text')
print (CO.reader('[$ColorName]My text[$/]'))
```

<!-- ![Screenshot 2020-11-18 124019](https://user-images.githubusercontent.com/56244233/99627674-0de9ee00-2a35-11eb-8baf-16499800f9de.jpg) -->
