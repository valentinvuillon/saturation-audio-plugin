This is a saturation VST plug-in made with Juce, usable in any DAW.  

 ![IMAGE!](pictures/picture1.png)
<p align="center">
Here is a picture of the plug-in used in Ableton Live
</p>



#### How the plug-in works:  
The sample $n$ of the output signal $out[n]$ is $f(in[n])$ with $in[n]$ the sample $n$ of the input signal and $f$ a waveshaping function which is a saturating function $f:  x\mapsto 
 -1$ if $x\leqslant -1, 1.5x-0.5x^{3}$ if $-1 \lt x \lt 1 ,1$ if $x \geqslant 1$.  
 
<p align="center">
  <img width="450" height="450" src="pictures/picture2.png">
</p>
<p align="center">
Waveshaping function in red, with the $x\mapsto 
 x$ function in blue for comparison
</p>

\
The definition of this function is done in DSP_functions.cpp.  

#### Commands of the plug-in
The plug-in has two knobs:

* "Input gain", multiplies the input signal by a constant before applying the waveshaping function.
* "Dry/Wet", allows to blend the output signal of the plug-in (wet signal) with the untouched input signal (dry signal).  

#### How to build the plug-in:  
* Install the Juce Projucer  
* Set up a default project for an audio plug-in  
* Replace the source code from the default project with the source code from this repository  
* Build the code to produce a VST3 plug-in  



