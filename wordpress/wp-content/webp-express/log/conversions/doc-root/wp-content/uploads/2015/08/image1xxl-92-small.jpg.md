WebP Express 0.17.2. Conversion triggered using bulk conversion, 2019-10-12 08:18:31

*WebP Convert 2.3.0*  ignited.
- PHP version: 7.0.33
- Server software: Apache

Stack converter ignited

Options:
------------
The following options have been set explicitly. Note: it is the resulting options after merging down the "jpeg" and "png" options and any converter-prefixed options.
- source: [doc-root]/wp-content/uploads/2015/08/image1xxl-92-small.jpg
- destination: [doc-root]/wp-content/webp-express/webp-images/doc-root/wp-content/uploads/2015/08/image1xxl-92-small.jpg.webp
- log-call-arguments: true
- converters: (array of 9 items)

The following options have not been explicitly set, so using the following defaults:
- converter-options: (empty array)
- shuffle: false
- preferred-converters: (empty array)
- extra-converters: (empty array)

The following options were supplied and are passed on to the converters in the stack:
- default-quality: 70
- encoding: "auto"
- max-quality: 80
- metadata: "none"
- near-lossless: 60
- quality: "auto"
------------


*Trying: cwebp* 

Options:
------------
The following options have been set explicitly. Note: it is the resulting options after merging down the "jpeg" and "png" options and any converter-prefixed options.
- source: [doc-root]/wp-content/uploads/2015/08/image1xxl-92-small.jpg
- destination: [doc-root]/wp-content/webp-express/webp-images/doc-root/wp-content/uploads/2015/08/image1xxl-92-small.jpg.webp
- default-quality: 70
- encoding: "auto"
- low-memory: true
- log-call-arguments: true
- max-quality: 80
- metadata: "none"
- method: 6
- near-lossless: 60
- quality: "auto"
- use-nice: true
- command-line-options: ""
- try-common-system-paths: true
- try-supplied-binary-for-os: true

The following options have not been explicitly set, so using the following defaults:
- alpha-quality: 85
- auto-filter: false
- preset: "none"
- size-in-percentage: null (not set)
- skip: false
- rel-path-to-precompiled-binaries: *****
- try-cwebp: true
- try-discovering-cwebp: true
------------

Encoding is set to auto - converting to both lossless and lossy and selecting the smallest file

Converting to lossy
Looking for cwebp binaries.
Discovering if a plain cwebp call works (to skip this step, disable the "try-cwebp" option)
- Executing: cwebp -version. Result: *Exec failed* (the cwebp binary was not found at path: cwebp)
Nope a plain cwebp call does not work
Discovering binaries using "which -a cwebp" command. (to skip this step, disable the "try-discovering-cwebp" option)
Found 0 binaries
Discovering binaries by peeking in common system paths (to skip this step, disable the "try-common-system-paths" option)
Found 1 binaries: 
- /usr/local/bin/cwebp
Discovering binaries which are distributed with the webp-convert library (to skip this step, disable the "try-supplied-binary-for-os" option)
Checking if we have a supplied precompiled binary for your OS (Darwin)... We do.
Found 1 binaries: 
- [doc-root]/wp-content/plugins/webp-express/vendor/rosell-dk/webp-convert/src/Convert/Converters/Binaries/cwebp-103-mac-10_14
Detecting versions of the cwebp binaries found
- Executing: /usr/local/bin/cwebp -version. Result: version: *1.0.3*
- Executing: [doc-root]/wp-content/plugins/webp-express/vendor/rosell-dk/webp-convert/src/Convert/Converters/Binaries/cwebp-103-mac-10_14 -version. Result: *Exec failed* (the cwebp binary was not found at path: [doc-root]/wp-content/plugins/webp-express/vendor/rosell-dk/webp-convert/src/Convert/Converters/Binaries/cwebp-103-mac-10_14)
Binaries ordered by version number.
- /usr/local/bin/cwebp: (version: 1.0.3)
Trying the first of these. If that should fail (it should not), the next will be tried and so on.
Creating command line options for version: 1.0.3
Quality of source is 90. This is higher than max-quality, so using max-quality instead (80)
The near-lossless option ignored for lossy
Trying to convert by executing the following command:
nice /usr/local/bin/cwebp -metadata none -q 80 -alpha_q '85' -m 6 -low_memory '[doc-root]/wp-content/uploads/2015/08/image1xxl-92-small.jpg' -o '[doc-root]/wp-content/webp-express/webp-images/doc-root/wp-content/uploads/2015/08/image1xxl-92-small.jpg.webp.lossy.webp' 2>&1

*Output:* 
Saving file '[doc-root]/wp-content/webp-express/webp-images/doc-root/wp-content/uploads/2015/08/image1xxl-92-small.jpg.webp.lossy.webp'
File:      [doc-root]/wp-content/uploads/2015/08/image1xxl-92-small.jpg
Dimension: 300 x 300
Output:    9452 bytes Y-U-V-All-PSNR 40.35 46.23 46.40   41.59 dB
           (0.84 bpp)
block count:  intra4:        245  (67.87%)
              intra16:       116  (32.13%)
              skipped:        54  (14.96%)
bytes used:  header:            117  (1.2%)
             mode-partition:   1197  (12.7%)
 Residuals bytes  |segment 1|segment 2|segment 3|segment 4|  total
  intra4-coeffs:  |    6883 |      61 |      29 |      19 |    6992  (74.0%)
 intra16-coeffs:  |      91 |       0 |      25 |      68 |     184  (1.9%)
  chroma coeffs:  |     892 |       8 |      12 |      19 |     931  (9.8%)
    macroblocks:  |      70%|       2%|       4%|      25%|     361
      quantizer:  |      24 |      17 |      12 |      11 |
   filter level:  |       8 |       4 |       2 |       2 |
------------------+---------+---------+---------+---------+-----------------
 segments total:  |    7866 |      69 |      66 |     106 |    8107  (85.8%)

Success
Reduction: 57% (went from 21 kb to 9 kb)

Converting to lossless
Looking for cwebp binaries.
Discovering if a plain cwebp call works (to skip this step, disable the "try-cwebp" option)
- Executing: cwebp -version. Result: *Exec failed* (the cwebp binary was not found at path: cwebp)
Nope a plain cwebp call does not work
Discovering binaries using "which -a cwebp" command. (to skip this step, disable the "try-discovering-cwebp" option)
Found 0 binaries
Discovering binaries by peeking in common system paths (to skip this step, disable the "try-common-system-paths" option)
Found 1 binaries: 
- /usr/local/bin/cwebp
Discovering binaries which are distributed with the webp-convert library (to skip this step, disable the "try-supplied-binary-for-os" option)
Checking if we have a supplied precompiled binary for your OS (Darwin)... We do.
Found 1 binaries: 
- [doc-root]/wp-content/plugins/webp-express/vendor/rosell-dk/webp-convert/src/Convert/Converters/Binaries/cwebp-103-mac-10_14
Detecting versions of the cwebp binaries found
- Executing: /usr/local/bin/cwebp -version. Result: version: *1.0.3*
- Executing: [doc-root]/wp-content/plugins/webp-express/vendor/rosell-dk/webp-convert/src/Convert/Converters/Binaries/cwebp-103-mac-10_14 -version. Result: *Exec failed* (the cwebp binary was not found at path: [doc-root]/wp-content/plugins/webp-express/vendor/rosell-dk/webp-convert/src/Convert/Converters/Binaries/cwebp-103-mac-10_14)
Binaries ordered by version number.
- /usr/local/bin/cwebp: (version: 1.0.3)
Trying the first of these. If that should fail (it should not), the next will be tried and so on.
Creating command line options for version: 1.0.3
Trying to convert by executing the following command:
nice /usr/local/bin/cwebp -metadata none -q 80 -alpha_q '85' -near_lossless 60 -m 6 -low_memory '[doc-root]/wp-content/uploads/2015/08/image1xxl-92-small.jpg' -o '[doc-root]/wp-content/webp-express/webp-images/doc-root/wp-content/uploads/2015/08/image1xxl-92-small.jpg.webp.lossless.webp' 2>&1

*Output:* 
Saving file '[doc-root]/wp-content/webp-express/webp-images/doc-root/wp-content/uploads/2015/08/image1xxl-92-small.jpg.webp.lossless.webp'
File:      [doc-root]/wp-content/uploads/2015/08/image1xxl-92-small.jpg
Dimension: 300 x 300
Output:    45546 bytes (4.05 bpp)
Lossless-ARGB compressed size: 45546 bytes
  * Header size: 2129 bytes, image data size: 43391
  * Lossless features used: PREDICTION CROSS-COLOR-TRANSFORM SUBTRACT-GREEN
  * Precision Bits: histogram=3 transform=3 cache=10

Success
Reduction: -108% (went from 21 kb to 44 kb)

Picking lossy
cwebp succeeded :)

Converted image in 377 ms, reducing file size with 57% (went from 21 kb to 9 kb)
