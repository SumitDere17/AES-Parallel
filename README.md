# AES-Parallel
## Introduction
Advanced Encryption Standard (AES) is a symmetric-key algorithm and is one of the strongest standards for electronic encryption in the world. 
It is widely used in software, hardware as well as in cloud applications. However, AES takes quite some time to encrypt messages especially when 
the number of users as well as the length of the text is quite large,
which is the case in cloud enviroments.

AES is parallelisable as it is a symmetric block ciper and the encryption of each block is independent of the other blocks and as a result this can be done in a parallel fashion.
The paper uses the concepts of _coalescing_ and _slicing_.
1. **Coalescing** : Putting together all the users' data together from the buffer to a contingous memory location.
2. **Slicing** : Dividing the coalesced data into equal parts so workload amongst threads is distributed evenly.

 * `CCS`  : CPU Coalescing and Slicing
 * `CCNS` : CPU Coalescing and no Slicing
 * `CNC`  : CPU no Coalescing and no Slicing  
All these algorithms have been implemented in this project and the results have been recorded, visualised and verified.

## Results


The code was executed and tested with a uniformly random dataset of 100 files to 1000 files. Each file had random data from 30KB to 150KB 
generated using a pseudo random generator.  

The results are concurrent with that of those published in the paper.  
