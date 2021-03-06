```
usage: planarconfig [--uids] [--fix] <file>|<directory>...

The planarconfig utility detects the actual planar configuration of
uncompressed pixel data of color images with Photometric Interpretation
RGB or YBR_FULL and optionally correct non matching values of attribute
Planar Configuration of the image.

For each processed file one of the characters:
p - no pixel data
c - compressed pixel data
m - monochrome (or palette color) pixel data
0 - detected color-by-pixel planar configuration, matching with value 0
    of attribute Planar Configuration
O - detected color-by-pixel planar configuration, NOT matching with value 1
    of attribute Planar Configuration
1 - detected color-by-plane planar configuration, matching with value 1
    of attribute Planar Configuration
I - detected color-by-plane planar configuration, NOT matching with value 0
    of attribute Planar Configuration
is written to stdout.
If an error occurs on processing a file, an E character is written to stdout
and a stack trace is written to stderr.

Options:
--uids   log SOP Instance UIDs of files with not matching value of attribute
         Planar Configuration in file 'uids.log' in working directory.
--fix    fix files with NOT matching value of attribute Planar Configuration
```
