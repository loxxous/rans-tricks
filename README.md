# rans-tricks
This repo contains a few branchless modifications to a traditional rans coder, as a result it's performance is within a few percent of FSE whilst supporting adaptive probabilities and using no platform specific intrinsics or assembly.
All of this is public domain, do whatever you want with it.

A small benchmark on enwik8, Ryzen 1700 @ 3.7ghz:

Implementation         | Encode speed | Decode speed|
-----------------------|--------------|-------------|
4-way interleaved rans trick | 340 MB/s     | 460 MB/s    |
4-way implicit rans trick   | 270 MB/s     | 400 MB/s    |
4-way interleaved rans standard| 250 MB/s     | 300 MB/s    |
4-way implicit rans standard| 225 MB/s     | 250 MB/s    |
FSE                    | 325 MB/s     | 440 MB/s    |
