# EXAMPLE42 PUPPET MODULES

Released under the terms of Apache2 licence

Official website:
http://www.example42.com

## IMPORTANT NOTICE:

The Example42 modules set is going to have some heavy modifications:

* The "old" modules are kept on this repository under the branch 1.0
  You will find only bug-fixed for the old style modules there.

* The "nextgen" modules, still under development and research are
  placed in the dedicated repository:
  https://github.com/example42/puppet-modules-nextgen
  Read http://www.example42.com/?q=NextGen for more info about them

* In the master branch of this repository I'm going to merge old and new
  modules: all the new modules are git submodules

The reason for this choice is that I need to test the new modules in a 
live environment and that, in the mid-term, this repository is going to
be converted totally to the next-gen module set.

Usage of old and new modules is rather different so I reccommend extreme
attention if you want to update your current local repository from the
upstream master (stick to 1.0 branch to avoid surprises).

If you don't intend to keep your local copy aligned to the upstream version
you won't have problems, though I reccommend to migrate to the new 
modules sooner or later.

## DIFFERENCES BETWEEN OLD AND NEW MODULES

The new modules are compatible only with Puppet versions > 2.6
They are also compliant with the next Puppet 2.8 version, when dynamic 
variables scoping is going to be be discontinued.

The new modules can be used as the old ones, "set variables and include the
class" or can be used as parametrized classes.

The main difference for the first approach is that only top scope variables
can be used (so either set them in a ENC or use tools like Hiera to
give them the values you need according to custom conditions).

The new modules allow much cleaner and separated customizations so that you
hardly need to modify them in order to add custom resources or redefine
existing ones.

Decommissioning or classes is now done via top scope variables or arguments 
of the main class (absent, disable, disableboot) and not including the relevant
sub-class.

Monitoring and firewalling abstraction and Puppi integration are still present,
while backup abrastion has been discontinued.
The new modules use an alternative approach to Puppi integration.
The Puppi module is going to remain unique and compatible for both the old and
the new modules, at least until the migration has been completed.

For any question contact me via GitHub or on http://www.example42.com

Alessandro Franceschi
Lab42
