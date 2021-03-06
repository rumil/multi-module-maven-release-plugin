Changelog
---------

## 1.1.0

* Bug fix: tags are now pushed before building so that in the event of failure, the next build will use an incremented build number. 
This is needed for cases where part of the build succeeded and some module(s) were uploaded to Nexus - re-uploading would cause an 
error if the build number is not incremented. 

### 1.0.2

* Bug fix: When a git repository is partially checked out and the report repo has tags that the local repo does not, it was possible that the
generated version number would clash with an existing tag.

### 1.0.1

* Feature: A list of `releaseProfiles` can now be set in the plugin config.
* Bug fix: Support cases where Windows would return `C:\` and `c:\` for different calls in some situations, causing no sub-modules to build.
* Bug fix: When one commit has multiple tags, the wrong one would sometimes be seen as the latest and cause the release to fail.

## 1.0.0

First stable release.