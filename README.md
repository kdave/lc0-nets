# lc0 nets wrappers

The `lc0` needs a file with the network to run, this typically needs to be set up manually in GUI tool or as UCI `WeightsFile` parameter, or on the command line as `--weights`. There are many networks suitable for playing for fun on human skill level, or fun to watch to compete against each other. Here you can find a tool to look up a few of them, download, and create a shell script wrapper that is a single file executable. This simplifies the setup for GUI.

## Quick start

After git checkout, run

    $ ./lc0-nets download
    $ ./lc0-nets genscripts

The first command will download all configured nets from the `lc0-nets.json` file. The size varies and is roughly 700MiB for all devices. The second comand generates scripts like `lc0-from-name`, where `from` is usually author of the net and `name` is a nickname of the network if it was generated for some skill level, its generation or sequence number.

## What's there

* all the `maia-bot` networks, estimated Elo level 1100-1900, note it should be limited to depth 1 (settings in GUI is `nodes` and time control does not matter), you can play against a bot using these nets on lichess too
* big networks from 'dkappe', `goodgyal`, `badgyal`, `meangyal`
* a recent `lc0` network, this changes all the time so you may need to update it yourself
  * big - best from run3 (T80)
  * mid - best from run1 (T78)
  * small - best from run2 (if active)

## Hardware

Best hardware for neural network calculations is GPU or other specialized hardware, but some of the networks are still reasonably usable on CPU. Namely the 'maia' nets don't need deep search.

## GUI

* cutechess
* nibbler
* chessx
* scid
* PyChess

## Sources

* dkappe
  * https://github.com/dkappe/leela-chess-weights
  * https://github.com/dkappe/leela-chess-weights/wiki/Bad-Gyal
* sergio v https://www.comp.nus.edu.sg/~sergio-v/t60/384x30/
* more lc0 networks https://lczero.org/dev/wiki/best-nets-for-lc0/
* maia nets https://github.com/CSSLab/maia-chess
* lc0 training site https://training.lczero.org/
