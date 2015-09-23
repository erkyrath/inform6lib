This is version 6/11z of the Inform library,
Copyright Graham Nelson 1993-2004, Andrew Plotkin 2004-2006
Full release notes and instructions are available at
http://www.inform-fiction.org
and
http://www.ifarchive.org/indexes/if-archiveXinfocomXcompilersXinform6.html

The Git repository for the Inform library is at
  https://github.com/DavidGriffith/inform6lib
The repository for this branch is at
  https://github.com/erkyrath/inform6lib/tree/i6lib-611z

The Inform 6 Library is licensed under either
1) The traditional Inform license as described by the DM4, or
2) The Artistic License 2.0 (see ARTISTIC).


This branch (labelled "6/11z") is a *very minor* update of Graham's
6/11 branch (released in 2004). I (Zarf) am releasing it for the sake of
history; I've had it sitting in my source directory for a decade. Might
as well get in on GitHub.

Features of 6/11z as compared to 6/11:

- Define the constant SERIAL_COMMAS to get the American-style (Oxford)
  comma in lists.
- Define the constant SKIP_MAGIC_ARTICLES to suppress Inform's
  auto-detection of whether "a" or "an" is appropriate for object
  names. This makes the game run very slightly faster, but you must
  then define an "article" property for each object that begins with
  a vowel.
- Define the constant INTERRUPT_MULTI_ACTION to permit interrupting
  multiple-object actions (such as "get all"). Set the global multiflag
  to false in an action routine to do this. (For single-object actions,
  multiflag is already false, so setting it this way has no effect.)
- Define the constant ALLOW_AFTERGAME_RETRY to permit resurrecting
  the player from the post-game prompt. Replace the AfterGameOver
  routine and add an option that prints an appropriate message, sets
  deadflag to 0, and returns. The game will resume after the fatal 
  action. (This is distinct from the UNDO response, which undoes the
  fatal turn.)

Note that these features must be activated by defining the appropriate
constant. Without these constants, 6/11z is exactly the same as 6/11.

The 6/11z branch is not under active development. It contains only the
handful of features that I implemented for _The Dreamhold_ in 2006.
(Dreamhold used the 6/10 library; I have ported the features forward to
6/11.) (Except for the USE_PARTINVENT feature. In 6/11, that can be
better handled by writing an invent property which checks c_style.)

6/11z does not fix any of the outstanding 6/11 bugs, nor will it. For
bug fixes and future updates, see David Griffith's 6/12 repository (in
progress).

