Catcoin Core integration/staging tree
=====================================

[![Build Status](https://travis-ci.org/tmagik/catcoin.svg?branch=master)](https://travis-ci.org/tmagik/catcoin)

https://bitbucket.org/catcoin/catcoin

Copyright (c) 2009-2014 Bitcoin Core Developers
Copyright (c) 2013-2014 Catcoin Core by Catoshi and his developer Troy

NOT READY YET
-------------
This version of Catcoin is a forward-port of the Catcoin blockchain into the 
mainline Bitcoin-core software from https://www.bitcoin.org

What is Catcoin?
----------------

Catcoin is an experimental new digital currency that enables instant payments to
anyone, anywhere in the world. Catcoin uses peer-to-peer technology to operate
with no central authority: managing transactions and issuing money are carried
out collectively by the network. Catcoin Core is the name of open source
software which enables the use of this currency.

If this sounds like Bitcoin, that's because we borrowed their code and made it
friendlier for felines.

License
-------

Catcoin Core is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Catcoin developers are much like cats. The are difficult or impossible to herd,
and occasional have both short and long ongoing catfights. If you'd like
something done for catcoin, we highly encourage you to do it yourself, or hire
a developer (and pay them in catcoin, of course)

If it is a *more complicated or potentially controversial* change, then be
prepared for a catfight, and start a discussion on the 
[issue tracker](https://bitbucket.org/catcoin/catcoin/issues), or bring it up
on #catoshi-dev on the freenode IRC network.


The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see [doc/developer-notes.md](doc/developer-notes.md)) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/bitcoin/bitcoin/tags) are created
regularly to indicate new official, stable release versions of Bitcoin.

Building
--------

on debian:
    sudo apt-get install mercurial build-essential libboost-dev libdb++-dev \
        libssl-dev libminiupnpc-dev libboost-filesystem-dev \
        libboost-system-dev libboost-program-options-dev \
        libboost-thread-dev libboost-test-dev
    ./autogen.sh && ./configure && make

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test on short notice. Please be patient and help out by testing
other people's pull requests, and remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code. Unit tests can be compiled and run (assuming they weren't disabled in configure) with: `make check`

[Travis-ci](https://travis-ci.org/tmagik/catcoin/) is currently being .. um ..
tested as an automated testing system. Further tests will be added if Catoshi
feels like it to do usefull things like run a suite of tests to evaluate 
different difficulty adjustment algorithms.

### Manual Quality Assurance (QA) Testing

Large changes should have a test plan, and should be tested by somebody other
than the developer who wrote the code.
See https://github.com/bitcoin/QA/ for how to create a test plan.

Translations
------------

Changes to translations as well as new translations can be submitted to
[Bitcoin Core's Transifex page](https://www.transifex.com/projects/p/bitcoin/).

Translations are periodically pulled from Transifex and merged into the git repository. See the
[translation process](doc/translation_process.md) for details on how this works.

**Important**: We do not accept translation changes as GitHub pull requests because the next
pull from Transifex would automatically overwrite them again.

Translators should also subscribe to the [mailing list](https://groups.google.com/forum/#!forum/bitcoin-translators).
