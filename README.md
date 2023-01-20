# olcs-laminas

List of OLCS Laminas dependencies that are common across all repos

see https://dvsa.atlassian.net/browse/VOL-3206 for info on how and why this repo was created

# versioning

Versions for this repo follow the approximate Laminas version we're targeting, so begin at 2.5.

These days, Laminas packages aren't all jumping version numbers at the same time, and indeed some are still on v2.
So in practice, "version we're targeting" is likely to mean the service manager version, since that's where most upgrade blockers are found.

The idea is that we'll now be able to upgrade our backend, internal or selfserve nodes as soon as they're compatible, by swapping the version of this repo.

# pushing tags to Nexus

As we'll be maintaining two sets of tags going forward (initially 2.5.x and 3.0.x) we won't be able to use the update dependency
Jenkins job, or the 4.206.x naming. Instead check out the relevant tag from gitlab and run this from the command line:

composer push (tag name)
