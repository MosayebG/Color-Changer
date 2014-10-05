#!/usr/bin/python

from PIL import Image
import sys

if ( len(sys.argv) < 6 ): 
    print "Usage: ./png_changer.py <input.png> <output.png> <0-255> <0-255> <0-255>"
    sys.exit(0)

img = Image.open(sys.argv[1])
img = img.convert("RGBA")
datas = img.getdata()

newData = []

for item in datas:
    if item[0] == 0 and item[1] == 0 and item[2] == 0:
        newData.append((int(sys.argv[3]), int(sys.argv[4]), int(sys.argv[5]), item[3]))
    else:
        newData.append(item)

img.putdata(newData)
img.save(sys.argv[2])
