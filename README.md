noflash
=======

Noflash can be used to play videos from various sites without requiring flash.
It can be used with mplayer, mpv, omxplayer, vlc, quvi, youtube-dl etc.

This script is a valid bash script, greasemonkey (gm) script, and an html page.
- As a bash script, becomes a web server accepting the following request types:
  - http[s]://*  -> Play a remote video extracted from URL.
  - file:*       -> Play a file or browse a directory.
  - key:*        -> Send key press to the player.
- Server has a web interface to control the player, submit URLs, browse files,
  or download a js bookmarklet or a gm script. Gm script pings the server with
  visited http pages. Js bookmarklet sends the current page when clicked on.

How to use it:
- On server, run this as a bash script (e.g. bash `basename $0`).
- On client (can be the same machine), go to http://$NOFLASH_SERVER:$NOFLASH_PORT
  and install the javascript bookmarklet and/or the greasemonkey script.
- With the gm script, videos from supported sites should start automatically as
  you browse.  If you prefer to use the js bookmarklet, click on it to initiate.
- Server binds to localhost only by default.  Change NOFLASH_SERVER to server's
  IP to be able to access and remote control it from other computers (clients).
- See http://www.cs.umn.edu/~oztekin/software/noflash for more information.
