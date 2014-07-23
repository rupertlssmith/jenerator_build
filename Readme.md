=== Build Instructions

This is a top-level build that can pull in all the components of Jenerator, and build them.

This can be done in two ways, by creating symlinks to the components, which are already cloned into the parent directory, or by cloning the components into directories under this one.

Directly cloning the components under this directory, is the simplest method:

    ./clone_modules
    mvn install -Pignore

If the components (junit_toolkit, lojix, jenerator and maven2_plugins) have already been cloned intothe parent directory, create symlinks to those directories within this one, then build:

    ./symlink_modules
    mvn install -Pignore

Note the '-Pignore' option is currently needed, as there are failing tests that need to be cleaned up.
