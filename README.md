# tjafix
A small script that might improve compatibility of Taikojiro files

The [TJA format][1] is not equally well supported by all players.
This script attempts to improve this situation
by normalizing certain constructions in the files.
Currently, the least-common-denominator player used to test output files
is [TJAPlayer for 3DS][2],
though others may be used in the future.

In order to run this program, you must have `awk` installed.
A common implementation is [Gawk][3].
If you have a TJA file called `song.tja`, you can clean it with:

    awk -f tjafix song.tja > song-fixed.tja

or, on a typical Unix-like system, simply:

    tjafix song.tja > song-fixed.tja

Then `song-fixed.tja` is perhaps more likely to be usable than the original.

Note that it appears that many TJA files are created by hand,
and so there are bound to be strange cases that this program
does not cover.

[1]: https://github.com/bui/taiko-web/wiki/TJA-format
[2]: https://github.com/togetg/TJAPlayer_for_3DS
[3]: https://www.gnu.org/software/gawk/gawk.html
