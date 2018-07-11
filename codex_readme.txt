Important Information
---------------------
These directories provide the final model output for the CODEX series of models
as described in Ireland, Scholz and Wood, 2011, MNRAS, 418, 114 and
Scholz, Ireland and Wood, 2014, A&A (arXiv1404.6735S).

File Formats
------------
All file formats are text files, compressed with gzip.

The first line gives a description of the model. 
The second gives the model "parent star" radius. All other radii 
are in terms of this unit (called R_p).
The third line gives the number of wavelengths and the number of radius 
points in the center-to-limb profiles.
The fourth line gives headings and units for the first 3 columns, then the
center-to-limb radius ordinate for the remaining columns in units of R_p
Subsequent line give:
a: The Wavelength of each row in microns.
b: The model luminosity per unit wavelength
c: The central intensity, with which the centre to limb profile should be 
normalized.
d: The center to limb profile, normalized to 1.0 at a radius of 0.0.

Importantly, individual center-to-limb profiles CAN NOT BE USED due to 
the opacity sampling method of these models. Average at least 10 rows
together, degrading the spectral resolution, in order to obtain usable 
center-to-limb profiles. This average must be weighted by their central 
intensities, e.g. the CLV in a rectangular bandpass with edges \lambda_1
and \lambda_2 is given by:

CLV_bp(r) = \Int_{\lambda_1}^{\lambda_2} I_0 (\lambda) CLV(r,\lambda) d\lambda


Directories
-----------
o54:		Four cycles of a 5400 L_sun omi-Cet like model.
R52:		Four cycles of a 5200 L_sun R Leo like model. This model
	    	does not provide a particularly good fit to R Leo, as discussed
		in the paper II (MNRAS 2011).
C50:		Four cycles of a 5000 L_sun R Cas like model.
R81:		Four cycles of a 8100 L_sun R Cas like model.
x54:		Three cycles of a 5400 L_sun subsolar metalicity model.
s54:		Selected models for the o54 series with S-star like abundances
		(see Scholz, Ireland and Wood 2014)

See the file "models" in each directory for a simple description of which 
model number has which phase. This file also provides some detail as to 
the shock locations in each model.
