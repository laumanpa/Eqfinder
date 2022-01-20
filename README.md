# Eqfinder
MATLAB GUI application for detection and localisation of earthquakes in mseed files.
## How to use it
### First use
If you want to detect and localise earthquakes in your mseed files for the first time you have to put the files for each station in a seperate folder inside the data-in folder. 
If you have more than one component you have to create a seperate "data-in" folder for every component. place the first component inside the "data-in" folder and the second and third
inside a folder with the name "data-in1" and "data-in2". 

After you put the data in the folder you have to create a new excel file with the coordinates of all you seismometer stations, like in the example file.

When you have all your files, you can start the application. Here you can specify all the parameters for the sta/lta algorithm and for the inversion process. Then you can choose 
the time interval in which you want to look for events. You also have to specify a input and output file name. This are the files in which the results are saved. If you use the application 
for the first time, the input file does not matter. But the result will be saved in the output file with the name, you choose. 

After you set all of your parameters, you can run the app. Now, if the sta/lta algorithm finds an event this will be displayed. Then the app will ask you, if you want to change 
the component of one of the displayed seismograms. If you for example want to see the component of the first seismogram (counting from the top), which is stored in the "data-in2" 
folder, you have to type in "12", otherwise, if you don't want to change anything, just type "n" and the click ok. Afterwards you have to choose a category for your event. If you did 
this you can zoom in on every seismogram. When you are ready, press enter. Then you can pick the P- and S-arrivaltimes (Beging from the top). Click left, where you think the arrival times are.
First click for the P- and then for the S-arrivaltime. If you are not shure, click right and the time won't be used. Do this for every seismogram. If you dont want to use the event at all
you can either give it the category "n" or make at least one click with your mouse wheel. After you picked all arrivaltimes app will calculate the hypocenter, with the method and parameters 
you chose. All result will be saved in your output folder.
### Localise old events
If you already picked arriveltimes and you have your results in an outfut folder. You can choose this folder as an input. Then you don't have to pick this arrival times again.
If you just want to localise this old events without looking for new ones in the seismograms, you can choose the option "Relocate known events" Then the app will calculate the new 
locations, using the old arrivaltimes. This of coures just makes sense, if you change somthing in your parameters or if you use another methode. 

There are two posible inversion methodes. A grid search fith an adaptive mesh and a iterative-linear Inversion methode. The grid search works for a two layer underground and the 
iterative-linear methode just works for an homogeneous underground.
### Show results again
If you want to see the locations of the events in a output file, you can use the option "Just show known events" This gives you a plot with all the events in this file, which have 
a small enough residue. 
