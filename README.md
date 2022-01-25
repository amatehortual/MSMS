# MSMS
Spatio-temporal saliency descriptor

Descriptor to capture relevant information in videos.
To use the descriptor, you have to request the password to amatehortual@unal.edu.co or edromero@unal.edu.co, and to cite the article ....
The main function to obtain the saliency is computeMotionSaliency.m, which is described as follows:


function [SaliencyMap]=computeMotionSaliency(sequence,deltat,volsal)

%% Parameters:

=====>>>> Input:

**sequence:**     3D or 4D matrix of the intensity images I(u,T), where the 
               last column corresponds to the time, i.e., T is 1,...,N, 
               being N the number of frames and u the spatial coordinates
               (2D or 3D) 

**deltat:**       scalar of the distance between times to be used in the 
               estimation of the saliency along the sequence. A deltat 
               equal 1 will use all the sequence, while a value of 2 will 
               use the half of the data

**volsal:**      vector MX1 that contains the indices of the sequence whose 
               saliency will be estimated 

=====>>>> Output:

**SaliencyMap:**  it is a struct array (SaliencyMap(Ns).value) with the 
               number of salient volumes (1,...,Ns=length(volsal)) of the 
               saliency images S(u,volsal) computed for each time of the 
               temporal sequence volsal 

