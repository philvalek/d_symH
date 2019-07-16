# d_symH
This project is to look at using simple machine learning to predict SymH. My purpose for doing this is to practice working with the python ML tools. There are already a good number of space weather prediction tools out here, and those are much more sophisticated that this will be. FOr example, see the mms.rice.edu/realtime/dials.html for some good examples. 

This model will be pretty simple. We know that geomagnetic storms start when the IMF turns southward. This results in increased reconnection and convection through the magnetosphere. For my model, I am going to use the OMNI time shifted IMF and solar wind values, and the current SymH value to predict DsymH, where the "new" variable DsymH will be the change in SymH from the last time step. This initial model is very simple in that it not using any information about the state of the magnetosphere except the currnt state of SymH. Lets See how it works out.

I'll grab the data from CDA Web (https://cdaweb.gsfc.nasa.gov/index.html/). Initially I am just going to grab the files by hand. I do have a python script where I automatically went and downloaded the data a month at a time, but there must have been some change to the website format since the code now crashes. I'll go take a look at that later.

Other things to look at in the future, I am going to use data from CDAWeb, so it will be realtively old. A production tool would need to ingest realtime data. Perhaps as a version two I'll update the code to use realtime data and make real time updates.
