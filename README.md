# Evaluate-Stellar-Cluster-SED
This repository contains a set of functions used to evaluate the SED of a stellar cluster to provide estimations of its age, metallicity, mass and V-band extinction. Two evaluations are made, one using a single-star BPASS v 2.2 model set and another using a binary BPASS v 2.2 model set. This code is provided as supplementary material to an investigation regarding the effects of accounting for binary-star interactions when evaluating the unresolved photometry of stellar clusters.

**********

Function: 
 - Agefit(mag, err)

Inputs:
 - mag  = [FUV, NUV, U, B, V, R, I, J, H, K, u, g, r, i, z, f300w, f336w, f435w, f450w, f555w, f606w, f814w], a 1 x 22 array containing    the apparent magnitudes in a range of spectral filters.
 - err, a 1 x 22 array containing the corresponding errors in the measurements of the apparent magnitudes.

Output:
 - a 1 x 4 array
   containing the average best-fit log(age/yrs) using a single-star and binary evaluation: [Average best-fit Single log(age), associated    uncertainty, Average best-fit Binary log(age), associated uncertainty]

**********

Function: 
 - Zfit(mag, err)
 
Inputs:
 - mag  = [FUV, NUV, U, B, V, R, I, J, H, K, u, g, r, i, z, f300w, f336w, f435w, f450w, f555w, f606w, f814w], a 1 x 22 array containing    the apparent magnitudes in a range of spectral filters.
 - err, a 1 x 22 array containing the corresponding errors in the measurements of the apparent magnitudes.

Output:
 - a 1 x 4 array containing the average best-fit log(Z) using a single-star and binary evaluation: [Average best-fit Single log(Z),        associated uncertainty, Average best-fit Binary log(Z), associated uncertainty]
 
**********
 
Function: 
 - Dustfit(mag, err, Amin)
 
Inputs:
 - mag  = [FUV, NUV, U, B, V, R, I, J, H, K, u, g, r, i, z, f300w, f336w, f435w, f450w, f555w, f606w, f814w], a 1 x 22 array containing    the apparent magnitudes in a range of spectral filters.
 - err, a 1 x 22 array containing the corresponding errors in the measurements of the apparent magnitudes.
 - Amin, a float containing the minimum V-band extinction of the object.

Output:
 - a 1 x 4 array containing the average best-fit V-band extinction using a single-star and binary evaluation: [Average best-fit Single      A_V, associated uncertainty, Average best-fit Binary A_V, associated uncertainty]
 
**********
 
Function: 
 - Massfitv1(mag, err, dmod)
 
Inputs:
 - mag  = [FUV, NUV, U, B, V, R, I, J, H, K, u, g, r, i, z, f300w, f336w, f435w, f450w, f555w, f606w, f814w], a 1 x 22 array containing      the apparent magnitudes in a range of spectral filters.
 - err, a 1 x 22 array containing the corresponding errors in the measurements of the apparent magnitudes.
 - dmod = [Distance modulus of stellar cluster, Uncertainty in distance modulus], a 1 x 2 array specifying the distance modulus and the    uncertainty in this measurement.

Output:
 - a 1 x 4 array containing the average best-fit log(Mass/M_solar) using a single-star and binary evaluation: [Average best-fit Single      log(Mass/M_solar), associated uncertainty, Average best-fit Binary log(Mass/M_solar), associated uncertainty]

**********

Function: 
 - Clusterfit(mag, err, Amin)

Inputs:
 - mag  = [FUV, NUV, U, B, V, R, I, J, H, K, u, g, r, i, z, f300w, f336w, f435w, f450w, f555w, f606w, f814w], a 1 x 22 array containing    the apparent magnitudes in a range of spectral filters.
 - err, a 1 x 22 array containing the corresponding errors in the measurements of the apparent magnitudes.
 - Amin, a float containing the minimum V-band extinction of the object.

Output:
 - a 1 x 12 array containing the average best-fit log(age/yrs), log(Z) and V-band extinction using a single-star and binary evaluation:    [Average best-fit Single log(age/yrs), associated uncertainty, Average best-fit Binary log(age/yrs), associated uncertainty, Average    best-fit Single log(Z), associated uncertainty, Average best-fit Binary log(Z), associated uncertainty, Average best-fit Single A_V,    associated uncertainty, Average best-fit Binary A_V, associated uncertainty]
 
**********
 
 Function: 
 - Massfitv2(mag, err, Amin, dmod)

Inputs:
 - mag  = [FUV, NUV, U, B, V, R, I, J, H, K, u, g, r, i, z, f300w, f336w, f435w, f450w, f555w, f606w, f814w], a 1 x 22 array containing    the apparent magnitudes in a range of spectral filters.
 - err, a 1 x 22 array containing the corresponding errors in the measurements of the apparent magnitudes.
 - Amin, a float containing the minimum V-band extinction of the object.
 - dmod = [Distance modulus of stellar cluster, Uncertainty in distance modulus], a 1 x 2 array specifying the distance modulus and the    uncertainty in this measurement.

Output:
 - a 1 x 8 array containing the average best-fit log(Mass/M_solar) and V-band extinction using a single-star and binary evaluation:        [Average best-fit Single log(Mass/M_solar), associated uncertainty, Average best-fit Binary log(Mass/M_solar), associated                uncertainty, Average best-fit Single A_V, associated uncertainty, Average best-fit Binary A_V, associated uncertainty]
