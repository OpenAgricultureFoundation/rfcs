## Formal process for developer workflow

* The `master` branch is the latest release.  ***No active development happens on it.***

* The `develop` branch starts as a branch from master and is permanent.  *This is where active development happens.*

* Any fixes or features happen on a temporary branch off of `develop`. They are PR’d back to `develop`.

* We drive `develop` to a stable, tested, working release then tag it with *vX.Y.Z*. 
  * When a release tag is made, the `develop` branch is merged back to `master` (which will have the same tag applied). 
  * We advertise to the community the new release is ready and provide release notes with a list of fixes/features.

* CI (continuous integration) is always running on master and develop. 
  * I suggest we also figure out how to make the Travis CI system email an “<user> broke the build with commit <id>” message to a dev list.

## Drawbacks
A bit more process that has been done before.

## Alternatives
Continue with the current `master` > `work` branch > PR back to `master` process.

## Deadline for comments
* Deadline for comments on this RFC is Monday 2017-06-12.
