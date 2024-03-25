![logo](https://i.ibb.co/5rdDr7p/header.png)

Python Image library for GASMIX EUDP Distro (PImGED) is used for handling image data collected 
during the experiments of the GASMIX project supported by EUDP, MAN ES and DTU. 

The framework is designed to handle large amounts of image data with limited computational 
resources. Several optimized function utilizing OpenCV C++, numba compilation and multithreading 
through the Joblib package, are used to speed-up computations and memory handling.

## [code pages are found here](https://benhartz.github.io/pimged-pages/)

## Installation

## Code structure
![codestructure](https://i.ibb.co/QbFw4RF/code-structure.png)


To handle larger data amounts the code takes inspiration from Panda on datastructure and 
implement a dataset module used for loading/saving data. The data is handled by datacontainers 
with functions for manipulating the individual datatypes. With the datacontainer module implementing
versatile classes for image and pressure datahandling, with common internal functions, it is 
possible to reduce code repetition and adding datacontainers to the module. The metadata from 
data is handled and stored for the individual dataset in the same datacontainer for and sent around 
with the data. The dataset module object is then used as an input for other modules that can use 
the standardrised data setup.
 
Handling standard calculations a calculation module takes the dataset object as an input. 
When new information is calculated it can then populate the dataset object with information, 
utilizing the indirection implementation of list and numpy arrays in python. This streamline the 
collection of data in one object that can load or save the data with minimal coding.

Between the whole framework, several functions are reused with simple coding and these are 
included in a utility package with the framework. Here is sorting of list elements widely used 
in folder and filenames, checking folder paths, handling metadata etc. 

Splitting the code framework into specialized modules decouple functionality and makes it 
easy to update individual functionality in different modules, without breaking code coherence.

---

## Support
The code is maintained during the GASMIX project from 2022 till start of 2025 by Benjamin Hartz

After project end there are no plans for further support of the code from main authors. 


## Authors and acknowledgment
Created by Benjamin Hartz

Created during the GASMIX PhD project at DTU Construct under FVM, supported by EUPD and MAN ES 

## License
[BSD 3-Clause License](LICENSE.txt)

Copyright (c) 2024, Benjamin Arnold Krekeler Hartz

---