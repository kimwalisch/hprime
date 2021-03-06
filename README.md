hprime
=============


A fast prime sieve.

Currently it is unoptimised for primes > ~10^10

URL:
-----

An explanation of some of the optimisations used in hprime can be found at:

http://tverniquet.com/hprime

To build run:
-------------

```
make
```

 - This is currently very simple and directly creates the binary `bin/hprime`.
 - The code will likely not compile without gcc (gcc-5).
 - It will likely not work on architectures other than modern x86_64.


My development machine is running ubuntu 15.10 with gcc-5 installed. When
testing I set the cpu frequency to performance using cpu-freq.


Usage:
-------

    hprime start_num end_num [plan] [num_threads] [in_order]
    
      start_num   - **broken** for anything other than 0
      end_num     - the number to count primes up to
      plan        - different methods. 0 (default) is fastest
      num_threads - 0 for true single-threaded
      in_order    - 1 to force a multithreaded run to count in order

History:
=========

There was a light-hearted challenge on the Australian forum website whirlpool.net, which was "who can make the fastest prime generator".

The challenge really sucked me in. When nothing I could do could make my sieve any faster, I'd suddenly get a little nibble and would see another speed increase and it would take my interest again.

So fast-forward 3 years and this is the result.
