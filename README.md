CateDoge integration/staging tree
================================

http://catedoge.com


What is CateDoge?
----------------

CateDoge is internet based P2P currency which uses Keccak (Sha3) as proof of work to secure the network. SHA-3 is reported to be very secure and its mineable by GPUs and CPUs. CateDoge has kimoto gravity well implemented from the start which prevents from multipools mining and dumping the coins.

 - 100000 CTD per block
 - Halves every 36,000 blocks
 - Minimum 12,500 coins until total of 20billion coins are mined
 - total of 20b coins approx
 - difficulty retarget: Kimoto gravity well
 - block: every 2 minutes
 
For more details and wallet downloads for windows, linux and mac please visit http://catedoge.com

License
-------

CateDoge is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the CateDoge
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion (if they haven't already) on the
[mailing list](http://sourceforge.net/mailarchive/forum.php?forum_name=bitcoin-development).

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags] are created
regularly to indicate new official, stable release versions of CateDoge.

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

    qmake CATEDOGE_QT_TEST=1 -o Makefile.test catedoge-qt.pro
    make -f Makefile.test
    ./CateDoge-qt_test

