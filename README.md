SMhasher
========

| Hash function                                 |      MiB/sec |cycl./hash|cycl./map   | size| Quality problems               |
|:----------------------------------------------|-------------:|---------:|-----------:|----:|--------------------------------|
| [donothing32](doc/donothing32)                |  14924689.47 |     6.00 |     -      |  13 | test NOP                       |
| [donothing64](doc/donothing64)                |  14942317.78 |     6.00 |     -      |  13 | test NOP                       |
| [donothing128](doc/donothing128)              |  14943678.61 |     6.00 |     -      |  13 | test NOP                       |
| [NOP_OAAT_read64](doc/NOP_OAAT_read64)        |     29794.83 |    35.50 |     -      |  47 | test NOP                       |
| [BadHash](doc/BadHash)                        |       522.75 |    96.39 |     -      |  47 | test FAIL                      |
| [sumhash](doc/sumhash)                        |      7135.41 |    31.14 |     -      | 363 | test FAIL                      |
| [sumhash32](doc/sumhash32)                    |     23873.87 |    22.49 |     -      | 863 | test FAIL                      |
| [multiply_shift](doc/multiply_shift)          |      4909.57 |    45.28 | too slow | 345 | fails all tests                |
| [pair_multiply_shift](doc/pair_multiply_shift)|     13604.46 |    31.71 | too slow | 609 | fails all tests                |
| --------------------------                    |              |          |            |     |                                |
| [crc32](doc/crc32)                            |       392.05 |   130.08 | 205.11 (10) | 422 | insecure, 8590x collisions, distrib |
| [md5_32a](doc/md5_32a)                        |       317.78 |   730.30 | 842.13 (18) |4419 | 8590x collisions, distrib |
| [sha1_32a](doc/sha1_32a)                      |       364.95 |  1470.55 |1794.16 (13)|5126 | collisions, 36.6% distrib |
| [sha2-224](doc/sha2-224)                      |       147.13 |  1354.81 |1589.92 (12)|     |               |
| [sha2-224_64](doc/sha2-224_64)                |       147.60 |  1360.10 |1620.93 (13)|     |               |
| [sha2-256](doc/sha2-256)                      |       147.80 |  1374.90 |1606.06 (16)|     | Moment Chi2 4 |
| [sha2-256_64](doc/sha2-256_64)                |       148.01 |  1376.34 |1624.71 (16)|     | Moment Chi2 7 |
| [rmd128](doc/rmd128)                          |       332.78 |   672.35 | 903.43 (13) |     |               |
| [rmd160](doc/rmd160)                          |       202.16 |  1045.79 |1287.74 (16)|     |               |
| [rmd256](doc/rmd256)                          |       356.57 |   638.30 | 815.39 (16) |     |               |
| [blake2s-128](doc/blake2s-128)                |       295.30 |   698.09 |1059.24 (51)|     |               |
| [blake2s-160](doc/blake2s-160)                |       215.01 |  1026.74 |1239.54 (11)|     |               |
| [blake2s-224](doc/blake2s-224)                |       207.06 |  1063.86 |1236.50 (20)|     |               |
| [blake2s-256](doc/blake2s-256)                |       215.28 |  1014.88 |1230.38 (28)|     |               |
| [blake2s-256_64](doc/blake2s-256_64)          |       211.52 |  1044.22 |1228.43 (8) |     |               |
| [blake2b-160](doc/blake2b-160)                |       356.08 |  1236.84 |1458.15 (12)|     |               |
| [blake2b-224](doc/blake2b-224)                |       356.59 |  1228.50 |1425.87 (16)|     |               |
| [blake2b-256](doc/blake2b-256)                |       355.97 |  1232.22 |1443.31 (19)|     | Sparse high 32-bit |
| [blake2b-256_64](doc/blake2b-256_64)          |       356.97 |  1222.76 |1435.03 (9) |     |               |
| [sha3-256](doc/sha3-256)                      |       100.58 |  3877.18 |4159.79 (37)|     |               |
| [sha3-256_64](doc/sha3-256_64)                |       100.57 |  3909.00 |4174.63 (16)|     |               |
| [hasshe2](doc/hasshe2)                        |      2357.32 |    76.10 | 172.41 (3) | 445 | insecure, Permutation,TwoBytes,Zeroes,Seed  |
| [crc32_hw](doc/crc32_hw)                      |      6292.63 |    30.38 | 204.19 (18)| 653 | insecure, 100% bias, collisions, distrib, machine-specific (x86 SSE4.2) |
| [crc32_hw1](doc/crc32_hw1)                    |     23382.53 |    36.84 | 192.63 (3) | 671 | insecure, 100% bias, collisions, distrib, machine-specific (x86 SSE4.2) |
| [crc64_hw](doc/crc64_hw)                      |      8387.01 |    29.96 | 145.10 (3) | 652 | insecure, 100% bias, collisions, distrib, machine-specific (x64 SSE4.2) |
| [fibonacci](doc/fibonacci)                    |      9462.17 |    33.52 | 743.62 (4) |1692 | zeros, fails all tests       |
| [FNV1a](doc/FNV1a)                            |       780.53 |    69.65 | 190.38 (2) | 204 | zeros, fails all tests       |
| [FNV1A_Totenschiff](doc/FNV1A_Totenschiff)    |      6235.86 |    36.56 | 188.56 (4) | 270 | zeros, fails all tests       |
| [FNV1A_Pippip_Yurii](doc/FNV1A_Pippip_Yurii)  |      6238.08 |    37.22 | 184.54 (3) | 147 | sanity, fails all tests      |
| [FNV1a_YT](doc/FNV1a_YT)                      |      9618.28 |    28.26 | 178.00 (4) | 321 | fails all tests              |
| [FNV2](doc/FNV2)                              |      6244.26 |    38.25 | 149.50 (2) | 278 | fails all tests              |
| [FNV64](doc/FNV64)                            |       791.82 |    69.82 | 159.31 (2) |  79 | fails all tests              |
| [fletcher2](doc/fletcher2)                    |     11809.88 |    26.85 | 315.44 (2) | 248 | fails all tests              |
| [fletcher4](doc/fletcher4)                    |     11973.55 |    26.94 | 316.74 (2) | 371 | fails all tests              |
| [bernstein](doc/bernstein)                    |       791.83 |    67.15 | 183.25 (3) |  41 | fails all tests              |
| [sdbm](doc/sdbm)                              |       785.84 |    67.02 | 178.65 (2) |  41 | fails all tests              |
| [x17](doc/x17)                                |       522.46 |    97.51 | 195.82 (4) |  79 | 99.98% bias, fails all tests |
| [JenkinsOOAT](doc/JenkinsOOAT)                |       446.57 |   142.43 | 225.28 (3) | 153 | 53.5% bias, fails all tests  |
| [JenkinsOOAT_pl](doc/JenkinsOOAT_perl)        |       442.05 |   120.53 | 336.30 (4) |  65 | 1.5-11.5% bias, 7.2x collisions, LongNeighbors |
| [MicroOAAT](doc/MicroOAAT)                    |       950.84 |    62.23 | 199.62 (4) |  68 | 100% bias, distrib           |
| [farsh32](doc/farsh32)                        |     14053.09 |    74.29 | 245.33 (3) | 944 | insecure: AppendedZeroes, collisions+bias, MomentChi2, LongNeighbors |
| [farsh64](doc/farsh64)                        |      7216.29 |   130.30 | 302.44 (3) | 944 | insecure: AppendedZeroes, collisions+bias, MomentChi2, LongNeighbors |
| [jodyhash32](doc/jodyhash32)                  |      1386.76 |    46.13 | 181.80 (2) | 102 | bias, collisions, distr, LongNeighbors |
| [jodyhash64](doc/jodyhash64)                  |      2765.84 |    40.89 | 178.44 (4) | 118 | bias, collisions, distr, LongNeighbors |
| [lookup3](doc/lookup3)                        |      1702.13 |    48.25 | 203.28 (2) | 341 | 28% bias, collisions, 30% distr  |
| [superfast](doc/superfast)                    |      1899.70 |    54.19 | 191.96 (3) | 210 | 91% bias, 5273.01x collisions, 37% distr, BIC |
| [MurmurOAAT](doc/MurmurOAAT)                  |       437.03 |   117.00 | 191.56 (3) |  47 | collisions, 99.998% distr., BIC, LongNeighbors |
| [Crap8](doc/Crap8)                            |      3060.17 |    35.25 | 198.15 (3) | 342 | 2.42% bias, collisions, 2% distrib |
| [Murmur2](doc/Murmur2)                        |      3032.69 |    41.97 | 175.72 (2) | 358 | 1.7% bias, 81x coll, 1.7% distrib, BIC |
| [Murmur2A](doc/Murmur2A)                      |      3033.56 |    46.63 | 190.52 (3) | 407 | 12.7% bias, LongNeighbors          |
| [Murmur2B](doc/Murmur2B)                      |      4728.94 |    47.90 | 156.66 (4) | 433 | 1.8% bias, collisions, 3.4% distrib, BIC |
| [Murmur2C](doc/Murmur2C)                      |      3817.99 |    47.67 | 167.62 (3) | 444 | 91% bias, collisions, distr, BIC, LongNeighbors |
| [Murmur3A](doc/Murmur3A)                      |      2347.90 |    51.38 | 180.62 (2) | 351 | Moment Chi2 69             |
| [PMurHash32](doc/PMurHash32)                  |      2281.97 |    58.65 | 208.84 (2) |1862 | Moment Chi2 69             |
| [Murmur3C](doc/Murmur3C)                      |      3093.46 |    68.53 | 199.89 (4) | 859 | LongNeighbors, DiffDist    |
| [xxHash32](doc/xxHash32)                      |      5868.40 |    49.08 | 175.66 (4) | 738 | LongNeighbors, collisions with 4bit diff, MomentChi2 220 |
| [metrohash64_1](doc/metrohash64_1)            |      9274.60 |    50.85 | 154.76 (2) | 624 | LongNeighbors, BIC         |
| [metrohash64crc_1](doc/metrohash64crc_1)      |     13641.79 |    56.19 | 152.33 (3) | 632 | cyclic collisions 8 byte, BIC, machine-specific (x64 SSE4.2) |
| [metrohash64crc_2](doc/metrohash64crc_2)      |     13550.77 |    56.17 | 163.91 (3) | 632 | cyclic collisions 8 byte, BIC, machine-specific (x64 SSE4.2) |
| [metrohash128crc_1](doc/metrohash128crc_1)    |     13668.29 |    85.94 | 202.16 (4) | 723 | machine-specific (x64 SSE4.2) |
| [metrohash128crc_2](doc/metrohash128crc_2)    |     13600.83 |    85.92 | 201.48 (2) | 723 | machine-specific (x64 SSE4.2) |
| [metrohash128_1](doc/metrohash128_1)          |      9263.64 |    79.71 | 190.85 (3) | 773 | LongNeighbors              |
| [metrohash128_2](doc/metrohash128_2)          |      9060.39 |    79.74 | 191.47 (4) | 773 | LongNeighbors              |
| [cmetrohash64_1o](doc/cmetrohash64_1o)        |      8851.32 |    50.59 | 162.37 (3) |3506 | LongNeighbors              |
| [cmetrohash64_1](doc/cmetrohash64_1)          |      9074.37 |    50.92 | 166.30 (5) | 652 | LongNeighbors              |
| [City64noSeed](doc/City64noSeed)              |      8873.07 |    38.70 | 182.06 (4) |1038 | Avalanche, Sparse, TwoBytes, MomentChi2, Seed |
| [City64](doc/City64)                          |      9213.05 |    55.52 | 201.39 (4) |1120 | Sparse, TwoBytes           |
| [falkhash](doc/falkhash)                      |     20374.98 |   169.84 | 333.37 (3) | 264 | LongNeighbors, machine-specific (x64 AES-NI) |
| [t1ha1_64le](doc/t1ha1_64le)                  |      9541.33 |    39.33 | 177.90 (2) | 517 | Avalanche                  |
| [t1ha1_64be](doc/t1ha1_64be)                  |      6848.76 |    41.08 | 192.00 (2) | 555 | Avalanche                  |
| [t1ha0_32le](doc/t1ha0_32le)                  |      4913.74 |    55.00 | 181.06 (2) | 509 | Sparse, LongNeighbors      |
| [t1ha0_32be](doc/t1ha0_32be)                  |      4241.68 |    55.12 | 183.53 (5) | 533 | Sparse, LongNeighbors      |
| [t1ha2_stream](doc/t1ha2_stream)              |      8558.73 |    93.45 | 249.84 (4) |1665 | Sparse, Permutation, LongNeighbors |
| [t1ha2_stream128](doc/t1ha2_stream128)        |      8846.52 |   117.19 | 272.11 (3) |1665 | Sparse, Permutation, LongNeighbors |
| [xxh3](doc/xxh3)                              |     11694.36 |    37.07 | 169.62 (2) | 744 | Moment Chi2 14974, BIC     |
| [xxh3low](doc/xxh3low)                        |     10664.58 |    36.96 | 198.01 (2) | 756 | Moment Chi2 1.8e+9 !       |
| [xxh128](doc/xxh128)                          |     11553.50 |    41.68 | 176.50 (3) |1012 | Moment Chi2 14974          |
| [xxh128low](doc/xxh128low)                    |     11482.39 |    37.60 | 173.03 (6) |1012 | Moment Chi2 14974, BIC     |
| --------------------------------------        |              |          |            |     |                            |
| [tifuhash_64](doc/tifuhash_64)                |        35.60 |  1679.52 |1212.75 (15)| 276 |                            |
| [SipHash](doc/SipHash)                        |       958.78 |   141.84 | 277.73 (8) |1071 |                            |
| [HalfSipHash](doc/HalfSipHash)                |       741.59 |   122.25 | 254.24 (4) | 700 | zeroes                     |
| [GoodOAAT](doc/GoodOAAT)                      |      1052.90 |    70.80 | 198.34 (9) | 237 |                            |
| [SipHash13](doc/SipHash13)                    |      1762.44 |   104.61 | 238.92 (5) | 778 | 0.9% bias                  |
| [TSip](doc/TSip)                              |      3346.72 |    60.02 | 215.12 (6) | 519 | !msvc                      |
| [seahash](doc/seahash)                        |      4517.87 |    65.03 | 199.88 (3) | 871 | !msvc                      |
| [seahash32low](doc/seahash32low)              |      4589.52 |    64.53 | 213.62 (5) | 871 | !msvc                      |
| [clhash](doc/clhash)                          |      4405.28 |    85.35 | 239.53 (4) |1809 | machine-specific (x64 SSE4.2) |
| [HighwayHash64](doc/HighwayHash64)            |      6239.64 |    98.65 | 258.06 (3) |2546 |                            |
| [Murmur3F](doc/Murmur3F)                      |      5076.20 |    51.66 | 180.99 (3) | 699 |                            |
| [fasthash32](doc/fasthash32)                  |      4658.24 |    50.50 | 196.04 (3) | 566 |                            |
| [fasthash64](doc/fasthash64)                  |      4657.64 |    47.71 | 168.41 (2) | 509 | Moment Chi2 5159 !         |
| [MUM](doc/MUM)                                |      6890.75 |    39.90 | 174.09 (2) |1912 | machine-specific (32/64 differs) |
| [MUMlow](doc/MUMlow)                          |      6893.98 |    46.02 | 189.36 (3) |1912 |                            |
| [mirhash](doc/mirhash)                        |      5453.50 |    42.31 | 161.95 (3) |1112 | LongNeighbors, machine-specific (32/64 differs) |
| [mirhash32low](doc/mirhash32low)              |      5452.48 |    42.31 | 190.94 (2) |1112 | LongNeighbors, machine-specific (32/64 differs) |
| [mirhashstrict](doc/mirhashstrict)            |      2217.70 |    65.39 | 176.98 (2) |1112 |                            |
| [mirhashstrict32low](doc/mirhashstrict32low)  |      2217.87 |    64.72 | 188.73 (3) |1112 | MomentChi2 9               |
| [City32](doc/City32)                          |      3833.52 |    52.97 | 211.50 (2) |1319 |                            |
| [City64low](doc/City64low)                    |      9209.88 |    63.55 | 219.42 (2) |1120|                             |
| [City128](doc/City128)                        |      9747.33 |    77.22 | 212.03 (3) |1841 |                            |
| [CityCrc128](doc/CityCrc128)                  |     12958.29 |    77.31 | 212.58 (3) | 295 |                            |
| [FarmHash32](doc/FarmHash32)                  |     16663.96 |    63.67 | 210.15 (4) |11489| machine-specific (x64 SSE4/AVX) |
| [FarmHash64](doc/FarmHash64)                  |      8476.56 |    65.05 | 208.46 (2) |3758 |                            |
| [FarmHash128](doc/FarmHash128)                |      9814.32 |    82.06 | 227.90 (3) | 163 |                            |
| [farmhash32_c](doc/farmhash32_c)              |     17335.51 |    63.77 | 223.20 (5) | 762 | machine-specific (x64 SSE4/AVX) |
| [farmhash64_c](doc/farmhash64_c)              |      8335.98 |    77.01 | 210.44 (3) |3688 |                            |
| [farmhash128_c](doc/farmhash128_c)            |     10158.20 |    98.80 | 232.88 (4) |1890 |                            |
| [metrohash64_2](doc/metrohash64_2)            |      9281.99 |    51.04 | 153.03 (3) | 627 | LongNeighbors              |
| [cmetrohash64_2](doc/cmetrohash64_2)          |      9302.98 |    51.09 | 160.74 (3) | 655 | LongNeighbors              |
| [xxHash64](doc/xxHash64)                      |      8719.19 |    59.22 | 169.10 (5) |1999 |                            |
| [Spooky32](doc/Spooky32)                      |      9570.40 |    70.27 | 195.86 (3) |2221 |                            |
| [Spooky64](doc/Spooky64)                      |      9603.18 |    70.19 | 187.07 (3) |2221 |                            |
| [Spooky128](doc/Spooky128)                    |      9865.67 |    70.84 | 195.57 (3) |2221 |                            |
| [t1ha2_atonce](doc/t1ha2_atonce)              |      8192.03 |    48.48 | 179.12 (5) | 541 |                            |
| [t1ha2_atonce128](doc/t1ha2_atonce128)        |      8382.53 |    64.15 | 198.89 (2) | 613 | LongNeighbors              |
| [t1ha0_aes_noavx](doc/t1ha0_aes_noavx)        |     21782.86 |    48.17 | 179.10 (3) | 925 | LongNeighbors, machine-specific (x86 AES-NI) |
| [t1ha0_aes_avx1](doc/t1ha0_aes_avx1)          |     22714.85 |    48.12 | 177.52 (2) | 843 | LongNeighbors, machine-specific (x64 AVX)    |
| [t1ha0_aes_avx2](doc/t1ha0_aes_avx2)          |     22345.33 |    44.38 | 556.47 (89)| 792 | LongNeighbors, machine-specific (x64 AVX2)   |
| [MeowHash](doc/MeowHash)                      |     36695.65 |    58.09 | 233.81 (3) |1764 | Sparse low32, machine-specific (x64 AES-NI)  |
| [MeowHash32low](doc/MeowHash32low)            |     17247.34 |    87.32 | 245.98 (3) |1764 | Sparse, machine-specific (x64 AES-NI)        |
| [wyhash](doc/wyhash)                          |      9377.14 |    29.14 | 168.06 (3) |1373 |                            |
| [wyhash32low](doc/wyhash32low)                |      9281.60 |    27.54 | 184.27 (2) |1373 | Moment Chi2 4.2            |

The [sortable table variant](http://rurban.github.io/smhasher/doc/table.html)

Summary
-------

I added some SSE assisted hashes and fast intel/arm CRC32-C and AES HW variants, but not the fastest
[crcutil](https://code.google.com/p/crcutil/) yet. See [our crcutil results](https://github.com/rurban/smhasher/blob/master/doc/crcutil).
See also the old [https://code.google.com/p/smhasher/w/list](https://code.google.com/p/smhasher/w/list).

So the fastest hash functions on x86_64 without quality problems are:

- wyhash v3
- t1ha2_atonce
- metrohash64crc (x86 only)
- FarmHash (_not portable, too machine specific: 64 vs 32bit, old gcc, ..._)
- Spooky32
- fasthash
- MUM/mir (_different results on 32/64-bit archs_)

Hash functions for symbol tables or hash tables typically use 32 bit
hashes, for databases, file systems and file checksums typically 64 or
128bit, for crypto now starting with 256 bit.

Typical median key size in perl5 is 20, the most common 4. Similar for all other dynamic languages.
See [github.com/rurban/perl-hash-stats](https://github.com/rurban/perl-hash-stats)

When used in a hash table the instruction cache will usually beat the
CPU and throughput measured here. In my tests the smallest `FNV1A`
beats the fastest `crc32_hw1` with [Perl 5 hash tables](https://github.com/rurban/perl-hash-stats). 
Even if those worse hash functions will lead to more collisions, the
overall speed advantage and inline-ability beats the slightly worse quality.
See e.g. [A Seven-Dimensional Analysis of Hashing Methods and its Implications on Query Processing](https://infosys.cs.uni-saarland.de/publications/p249-richter.pdf)
for a concise overview of the best hash table strategies, confirming that the
simplest Mult hashing (bernstein, FNV*, x17, sdbm) always beat "better" hash
functions (Tabulation, Murmur, Farm, ...) when used in a hash table.

The fast hash functions tested here are recommendable as fast for file
digests and maybe bigger databases, but not for 32bit hash tables.  The
"Quality problems" lead to less uniform distribution, i.e.  more collisions
and worse performance, but are rarely related to real security attacks, just
the 2nd sanity zeroes test against `\0` invariance is security relevant.

Columns
-------

MiB/sec: The average of the Bulk key speed test for alignments 0-7 with 262144-byte keys.
The higher the better.

cycl./hash: The average of the Small key speed test for 1-31 byte keys.
The smaller the better.

cycl./map: The result of the Hashmap test for /usr/dict/words with
std::unordered_map get queries, with the standard deviation in
brackets. This tests the inlinability of the hash function (see size).
The smaller the better.

size: The object size in byte on AMD64. This affects the inlinability in e.g. hash tables.
The smaller the better.

Quality problems: See the failures in the linked doc.
The less the better.

Other
-----

* http://nohatcoder.dk/2019-05-19-1.html gives a new, useful hash level classification 1-5.
* [http://www.strchr.com/hash_functions](http://www.strchr.com/hash_functions) lists other benchmarks and quality of most simple and fast hash functions.
* [http://bench.cr.yp.to/primitives-hash.html](http://bench.cr.yp.to/primitives-hash.html) lists the benchmarks of all currently tested secure hashes.
* The [Hash Function Lounge](http://www.larc.usp.br/~pbarreto/hflounge.html) overviews the known weaknesses and attacks.


SECURITY
--------

The hash table attacks described in [SipHash](https://131002.net/siphash/)
against City, Murmur or Perl JenkinsOAAT or at
[Hash Function Lounge](http://www.larc.usp.br/~pbarreto/hflounge.html)
are not included here.

Such an attack avoidance cannot be the problem of the hash
function, but only the hash table collision resolution scheme.  You can
attack every single hash function, even the best and most secure if
you detect the seed, e.g. from language (mis-)features, side-channel
attacks, collision timings and independly the sort-order, so you need
to protect your collision handling scheme from the worst-case O(n),
i.e. separate chaining with linked lists. Linked lists chaining allows
high load factors, but is very cache-unfriendly.  The only
recommendable linked list scheme is inlining the key or hash into the
array. Nowadays everybody uses fast open addressing, even if the load
factor needs to be ~50%, unless you use Cuckoo Hashing.

I.e. the usage of SipHash for their hash table in Python 3.4, ruby,
rust, systemd, OpenDNS, Haskell and OpenBSD is pure security theatre.
SipHash is not secure enough for security purposes and not fast enough
for general usage. Brute-force generation of ~32k collisions need 2-4m
for all these hashes. siphash being the slowest needs max 4m, other
typically max 2m30s, with <10s for practical 16k collision attacks
with all hash functions.  Using Murmur is usually slower than a simple
Mult, even in the worst case.  Provable secure is only uniform
hashing, i.e. 2-5 independent Mult or Tabulation, or using a
guaranteed logarithmic collision scheme (a tree) or a linear collision
scheme, such as Robin Hood or Cockoo hashing with collision counting.

One more note regarding security: Nowadays even SHA1 can be solved in
a solver, like Z3 (or faster ones) for practical hash table collision
attacks (i.e. 14-20 bits). So all hash functions with less than 256
bits tested here cannot be considered "secure" at all.

The '\0' vulnerability attack with binary keys is tested in the 2nd
Sanity Zero test.

CRYPTO
------

The official NIST hash function testsuite does not do such extensive
statistical tests, to search for weak ranges in the bits. Also crypto
does not change the initial state, which we do here for our random
32bit seed. Crypto mostly cares about unreversable key -> hash
functions without changing the initial fixed state and
timings/sidechannel attacks.

The NIST "Cryptographic Algorithm Validation Program" (CAVP) involves
the testing of the implementations of FIPS-approved and
NIST-recommended cryptographic algorithms. During the NIST SHA-3
competition, the testing methodology was borrowed from the "CAVP",
as the KATs and MCTs of the [SHA-3 Competition Test Suite](https://csrc.nist.gov/CSRC/media/Projects/Cryptographic-Algorithm-Validation-Program/documents/sha3/sha3vs.pdf)
were based on the CAVP tests for SHA-2. In addition to this, the “Extremely Long
Message Test,” not present in the CAVP for SHA-2, required the
submitters to generate the hash value corresponding to a message with
a length of 1 GiB. “NIST - Cryptographic Algorithm Validation Program (CAVP),”
June 2017. Available: http://csrc.nist.gov/groups/STM/cavp
(No testing source code provided, just high-level descriptions)

Two other independent third party testsuites found an extensive number
of bugs and weaknesses in the SHA3 candidates.
"Finding Bugs in Cryptographic Hash Function Implementations",
Nicky Mouha, Mohammad S Raunak, D. Richard Kuhn, and Raghu Kacker, 2017.
https://eprint.iacr.org/2017/891.pdf

Maybe independent researchers should come together to do a better
public SHA-4 round, based on better and more testing methods, open
source code for the tests, and using standard industry practices, such
as valgrind, address-sanitizer and ubsan to detect obvious bugs.
