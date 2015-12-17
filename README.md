## travis_wait
:zzz: Increase timeout to your needs. More options to customize behaviour are available

### Usage

#### Examples

```sh
# Show output every minute, stop task after 40 minutes, 
# exit with code 0 (success), append output to existing logfile
./travis_wait -i 60 -l 2400 -x 0 -a 1 "make -j2 v=S" "build.log"
```

#### Options

```
  Usage: travis_wait [options] <command> [<logfile>]

  Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
  incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
  quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
  consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
  cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat
  non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

  Arguments:
    <command>       Slowpoke command
    <logfile>       Where <command>'s output will be saved
                    Default: $RANDOM-output.log
  Options:
    -i, --interval <int>   Refresh interval in sec.
                           Default: 30
                           
    -l, --limit <int>      Limit execution time in sec.
                           Default: 0 (Off)
                           
    -x, --exit-code <int>  Force the exit code
                           Default: -1 (Off)
                           
    -a, --append <int>     PRN append output to existing logfile
                           Off: 0 (Default)
                           On:  1
                           
    -h                     This help screen
```

### Related Docs
* [Build Timeouts](https://docs.travis-ci.com/user/customizing-the-build/#Build-Timeouts)
* [Build times out because no output was received](https://docs.travis-ci.com/user/build-timeouts#Build-times-out-because-no-output-was-received)
* [Notes from Whonix](https://www.whonix.org/wiki/Dev/Continuous_Integration)
