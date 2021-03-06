### 3.14.3

* OPTION_SKIP_MULLE_BOOTSTRAP is default NO if it looks like there was never a bootstrap

### 3.14.2

* Various small improvements

## 3.14.0

* depends on mulle-bootstrap 3.14 for tmp mechanism functions


### 3.13.3

* improve -V trace and environment dump

### 3.13.2

* fix --homebrew not building dependencies (or will I regret this soon) ?

### 3.13.1

* use ninja for sublime

## 3.13.0

* add mulle-sublime (mulle-build -sublime) to the commands


### 3.12.3

* use --no-build also for tests

### 3.12.2

* MAKEFLAGS and CMAKEFLAGS instead of MAKE_FLAGS and CMAKE_FLAGS for cultural compliance

## 3.12.0

* improve mingw compatibility

## 3.11.0

* improve working with multiple Xcode projects


### 3.9.2

* fix URL install and travis

### 3.9.1

* specify different or multiple rebuild files to watch with .dependencies.inc

## 3.9.0

* cleaned up a lot of options, some old favorites may be gone
* improved install


## 3.8.1

* check if src/dependencies.inc has been changed by the build, and if yes
rebuild once more

## 3.8.0

* when installing or homebrewing, **mulle-install** always trys to mirror git repos
if only temporary for the sake of faster fetches
* also cleanup test directory build folders, still need something to clean
tests output
* wipe the cmake cache, if any CMake*.txt files have been edited. Hopefully
this avoids a lot of grief I am suffering... :)
* add --no-bootstrap --build-dir options to use mulle-build to be run in
build-test.sh


### 3.7.0

* pass --debug to run-test
* never skip bootstrap when doing mulle-install
* fixed some typos

3.6.4
=====

* fixed `version`
* added `minimum-bootstrap-version` for packaging
* added CMakeLists.txt for packaging on Linux


3.6.3
=====

* run_install is a little more complex than I remembered...

3.6.2
=====

* fix install

3.6.0
=====

* keep version number similiar to mulle-bootstrap


3.4.1
=====

* Improve finding of the tests folder.
* mulle-build --tests-path will output the tests folder path
* Improve output of paths from ./run-test.sh
* mulle-update is too dangerous and it's a goner


3.1.0
=====

Keep version in lockstep with mulle-bootstrap for the moment.

3.0.0
=====

Lot's of changes to be in lock-step with mulle-bootstrap. One nice feature
gained is mulle-analyze (you need mulle-scan-build or scan-build) for it to
work.

0.10.5
=====

More stupidity fixes..

0.10.4
=====

Aimless dicking around with --prefix and --homebrew, because I am kind of
on holiday and brain is turned off. Sorry.


0.10.3
=====

Fix a version check

0.10.2
=====

--homebrew and --prefix are no mutually incompatible, which makes
the most sense.

0.10.1
=====

--homebrew option needs to be after --prefix for linuxbrew
compatibility.


0.10.0
=====

Depends now on mulle-bootstrap 2.5 and incorporates internal changes to
support it.
mulle-install is now more efficient installing single libraries, that do
not need to fetch the dependencies.

--no-build-dependencies does not imply --no-install-dependencies anymore.


0.9.2
=====

* the -e option now also adds the prefix/include and prefix/lib directories
to the search path.


0.9.1
=====

* fix --homebrew flag for linux

0.9.0
=====

* use eval exekutor for cmake/make to protect parameters
* add --homebrew switch to fix mulle-clang builds inside homebrew


0.8.2
=====

* protect homebrew shims from PATH shenanigans
* improve fail output


0.8.1
=====

* pass all flags -D*|-W* to cmake

0.8.0
=====

* mulle-build assumes mulle-bootstrap is installed besides it, if it is, that
becomes its preferential path for it
* allow to specify cmake commandline flags with -DCMAKE (will not get passed
to mulle_bootstrap)
* add --dump-environment as a debug option

0.7.0
=====

* adapt to mulle-bootstrap 2.4.0

0.6.1
=====

* pass --debug to ./build-test.sh

0.6
=====

* added mulle-status, because I use it so often
* adapt to changes in mulle-build


0.5.3
=====

* mulle-update is more verbose and better at detecting remotes, who are not
named "origin"

0.5.2
=====

* be more verbose when tagging

0.5.1
=====

* fix use of CMAKE_INSTALL_PREFIX
* remove some unnecesary refresh calls to make things go faster

0.5
===

Mostly changes how flags are interpreted and passed to mulle-bootstrap.

* change -nb flag to -nbd

0.4
===

* Much improved documentation
* Fix mulle-clean a bit

0.3
===

* base code on mulle-bootstrap library functions for exekutor and logging
* add multiple options
* check for mulle-bootstrap version
* rename project from mulle-install to mulle-build
* do local command first, mulle-bootstrap later (f.e. for tagging). That way
more numerous local failures don't dirty dependencies.
* this version needs to be pushed out now, because I need it in travis.yml

0.2
===

* allow to specify a tag and a scm for URL install
