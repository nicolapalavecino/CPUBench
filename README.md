# cpubench.c

## A simple CPU Benchmarking tool

Author: Suyash Srijan<br />
Email: suyashsrijan@outlook.com<br />

This program calculates how much time your CPU takes to compute n digits of PI using [Chudnovsky Algorithm](http://en.wikipedia.org/wiki/Chudnovsky_algorithm) and n [prime numbers](http://en.wikipedia.org/wiki/Prime_number)
and uses the GNU Multiple Precision Arithmetic Library for most of the computations.

### Compiling
To compile in a linux environment (Ubuntu or Raspbian) install the necessary libraries doing:
```
sudo apt-get install libgmp3-dev
sudo apt-get install libssl-dev
```

Then compile doing:
```
gcc -O3 -Wall -o cpubench cpubench.c -lgmp -lssl -lcrypto -fopenmp
```

You can now run your own benchmark with `sudo ./cpubench <number> <options>`. An example of this is `sudo ./cpubench 5000 --singlethreaded --nodigits`.

