php-sepa-xml
============

Master: [![Build Status](https://api.travis-ci.org/MartinStefani/php-sepa-xml.png?branch=master)](http://travis-ci.org/MartinStefani/php-sepa-xml)

##Important notes about this fork
* This fork adds the possibility to add the creditor's address to the XML. This is optional and the nodes are not
generated if the addresses are not given.
* This is used on a production environment using pain.001.001.03 with the Slovenian bank NKBM.
* I will add a pull request upstream after covering the new functionality with test cases.
* Be aware, the ISO standard requires only ASCII characters and the StringHelper class takes care only of a bunch of characters.
I have added slovenian characters, but polish, hungarian etc. characters are missing.

##Description
SEPA file generator for PHP.

Creates an XML file for a Single Euro Payments Area (SEPA) Credit Transfer and Direct Debit.

License: GNU Lesser General Public License v3.0


The versions of the standard followed are:
* _pain.001.002.03_ (or _pain.001.001.03_) for credits
* and _pain.008.002.02_ (or _pain.008.001.02_) for debits

Institutions and associations that should accept this format:
* Deutsche Kreditwirtschaft
* Fédération bancaire française
* Nova KBM, Slovenia

However, always verify generated files with your bank before using!


##Installation
###Composer
This library is available in packagist.org, you can add it to your project
via Composer.

In the "require" section of your composer.json file:

Always up to date (bleeding edge, API *not* guaranteed stable)
```javascript
"digitick/sepa-xml" : "dev-master"
```

Specific version, API stability
```javascript
"digitick/sepa-xml" : "1.1.*"
```

## Documentation

* [handling Direct Debit](doc/direct_debit.md)
* [handling Direct Credit](doc/direct_credit.md)
