openSquat
====

[![Codacy Badge](https://api.codacy.com/project/badge/Grade/9231646e8ddf4efc9fb1f62f628df34a)](https://www.codacy.com/manual/atenreiro/opensquat?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=atenreiro/opensquat&amp;utm_campaign=Badge_Grade)
[![Build Status](https://travis-ci.com/atenreiro/opensquat.svg?branch=master)](https://travis-ci.com/atenreiro/opensquat)

![alt text](https://raw.githubusercontent.com/atenreiro/opensquat/master/screenshots/openSquat.PNG)

What is openSquat?
-------------

openSquat is an opensource Intelligence (OSINT) security project to identify **cyber squatting** threats to specific companies or domains, such as:

*  Domain squatting
*  Typo squatting
*  IDN homograph attacks
*  Phishing
*  Doppenganger domains
*  Scams

It does support some key features such as:

*  Automatic newly registered domain updating (once a day)
*  Levenshtein distance to calculate word similarity
*  IDN homograph attack detection
*  Use different levels of confidence threshold to fine tune
*  Save output into different formats (txt, JSON and CSV)
*  Can be integrated with other threat intelligence tools and DNS sinkholes

This is an opensource project so everyone's welcomed to contribute.


Installation
------------

```bash
    $ git clone https://github.com/atenreiro/opensquat
    $ pip3 install -r requirements.txt
```

Make sure you have Python 3.6+ and pip3 in your environment

Usage Examples
------------

```bash
    # Lazy run with default options
    $ python3 main.py

    # for all the options
    $ python3 opensquat.py -h
    
    # With DNS validation (quad9)
    $ python3 main.py --dns quad9
    
    # Save output as JSON
    $ python3 main.py -o example.json -t json
    
    # Save output as CSV
    $ python3 main.py -o example.csv -t csv
    
    # Conduct a doppelganger validation
    $ python3 main.py --doppelganger_only
    
    # Search for registrations for over the last month (default: week)
    $ python3 main.py -p month
    
    # Tweak confidence level. The lower values bring more false positives
    # (0: very high, 1: high (default), 2: medium, 3: low, 4: very low
    $ python main.py -c 2 

```

To Do / Roadmap
-------------
*  Integration with VirusTotal (VT)
*  ~~Use certificate transparency~~
*  ~~Homograph detection~~ done
*  Improve code quality from B to A grade (codacy)
*  PEP8 compliance
*  Add documentation 

For more details check the [(Project)](https://github.com/atenreiro/opensquat/projects) section.

Changelog
-------------
*  Check the [CHANGELOG](https://github.com/atenreiro/opensquat/blob/master/CHANGELOG) file.

Authors
-------------
Project founder
*  Andre Tenreiro [(LinkedInk)](https://www.linkedin.com/in/andretenreiro/)
*  andre@cert.mz

Contributors
*  Please check the contributors page on GitHub

You can help this project by:
*  Providing your time and coding skills to enhance the project
*  Provide access to OSINT feeds
*  Open new issues with new ideas, bug report or feature proposals
*  Spread this project within your network
