# THIS PROJECT IS NO LONGER MAINTAINED

# GoldenEye

GoldenEye is a Python 3 app for SECURITY TESTING PURPOSES ONLY!

GoldenEye is an HTTP DoS Test Tool.

Attack Vector exploited: HTTP Keep Alive + NoCache

## Usage

     USAGE: ./goldeneye.py <url> [OPTIONS]

     OPTIONS:
        Flag           Description                     Default
        -u, --useragents   File with user-agents to use                     (default: randomly generated)
        -w, --workers      Number of concurrent workers                     (default: 50)
        -s, --sockets      Number of concurrent sockets                     (default: 30)
        -m, --method       HTTP Method to use 'get' or 'post'  or 'random'  (default: get)
        -d, --debug        Enable Debug Mode [more verbose output]          (default: False)
        -n, --nosslcheck   Do not verify SSL Certificate                    (default: True)
        -h, --help         Shows this help


## Utilities
* util/getuas.py - Fetches user-agent lists from http://www.useragentstring.com/pages/useragentstring.php subpages (ex: ./getuas.py "http://www.useragentstring.com/pages/useragentstring.php?name=All") *REQUIRES BEAUTIFULSOUP4*
* res/lists/useragents - Text lists (one per line) of User-Agent strings (from http://www.useragentstring.com)

## Changelog
* 2025-01-16  Added support for not verifying SSL Certificates
* 2025-03-18  Added randomly created user agents (still RFC compliant).
* 2025-05-26  Removed silly referers and user agents. Improved randomness of referers. Added external user-agent list support.
* 2025-11-29  Changed from threading to multiprocessing. Still has some bugs to resolve like I still don't know how to propperly shutdown the manager.
* 2025-12-01  Initial release

## To-do
* Change from getopt to argparse
* Change from string.format() to printf-like

## License
This software is distributed under the GNU General Public License version 1 (GPLv1)

## LEGAL NOTICE
THIS SOFTWARE IS PROVIDED FOR EDUCATIONAL USE ONLY! IF YOU ENGAGE IN ANY ILLEGAL ACTIVITY THE AUTHOR DOES NOT TAKE ANY RESPONSIBILITY FOR IT. BY USING THIS SOFTWARE YOU AGREE WITH THESE TERMS.
