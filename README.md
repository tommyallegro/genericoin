# genericoin
Genericoin integration/staging tree
================================

http://www.genericoin.org/

Copyright (c) 2009-2014 Bitcoin Developers
Copyright (c) 2011-2014 Litecoin Developers
Copyright (c) 2018 Genericoin Developers

What is Genericoin?
----------------
Genericoin is an experimental new digital currency that enables instant payments to anyone, 
anywhere in the world. Genericoin uses peer-to-peer technology to operate with no central authority: 
managing transactions and issuing money are carried out collectively by the network.
Genericoin Core is the name of open source software which enables the use of this currency.

For more information, as well as an immediately useable, binary version of the Genericoin Core software, see http://www.genericoin.org/

Genericoin is a lite version of Bitcoin using scrypt as a proof-of-work algorithm.
 - 3.0 minute block targets
 - subsidy halves in 420k blocks (~2 years)
 - ~164 million total coins

Genericoin has the following
 - 40 coins per block
 - 2016 blocks to retarget difficulty
The rest is the same as Bitcoin.


License
-------

Genericoin is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Genericoin
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion with the devs and community.

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/tommyallegro/genericoin/tags) are created
regularly to indicate new official, stable release versions of Genericoin.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test bitcoin-qt.pro
    make -f Makefile.test
    ./genericoin-qt_test
