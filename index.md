##Automating Map Production with Google Earth and ArcPy

---

We use Python to perform repetitive tasks

---

Unpack a zip of shapefiles, re-project them, and load into an SDE geodatabase

---

Geocode addresses based on a table that is updated daily

---

Python makes life easier, but…

---

Sometimes we can’t automate everything

---

This brings us to a challenge I once faced...

---

<center><p>Parcel Maps</p><img src="http://chan.indulgencelabs.com/img/Area_of_Interest2.jpg" style="width:35%;height:35%;" alt="alt text" title="Hastily Made Map" /></center>

---


![](http://chan.indulgencelabs.com/img/Area_of_Interest2.jpg)

---

The steps to create this map would be something like-

---

Add parcel layer, select parcels, export to shapefile, add to map, add basemap, symbolize layer...

---

...create layout, set map scale, add north arrow, add scale bar, add title, add date...

---

...save mxd (navigate to folder), export to pdf (navigate to folder again), open PDF, and...

---

...start over when you realize you forgot to select that one adjacent parcel

---

![](http://chan.indulgencelabs.com/img/missedParcel.jpg)

---

The steps involved in making this map could take 45-60 minutes

---

<5 minutes using Python and Google Earth

---

(My personal best is 1:15)


---

Demo

---

What was Python doing when the script executed?

---

![](http://chan.indulgencelabs.com/img/parcelScript.jpg)

---

Converted KML to layer, converted layer to shapefile, opened MXD template containing Parcel dataset, perform select by location...

---

...extract overlapping parcels, clear selection, add selected parcels to MXD, remove parcel layer...

---

...style parcel layer based on LYR file, set map scale by zooming to layer extent...

---

...save MXD, export as PDF, open PDF, quit

---

The bottom line: Python is doing a lot of work so you don't have to

---

REQUIREMENTS

---

Google Earth & Python

---

(duh)

---

MXD template containing layout

---

LYR template containing style

---

Parcel layer for selection

---

KML file for selecting from parcel layer

---

Python GUI Library: Tkinter (included with Python)

---

DRAWBACKS

---

Have to draw & save polygon as KML

---

Hard coded

---

Have to create the MXD and LYR templates ahead of time

---

How could it be expanded?

*Landscape vs Portrait Orientation

*User selects scale

*User defines where to find template files

---

So all you're really doing is creating a KML

---

Python does all the heavy lifting

