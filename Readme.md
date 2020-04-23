## go-update

Package update provides tooling to auto-update binary releases
from GitHub based on the user's current version and operating system. Used by command-line tools such as [Up](https://github.com/apex/up) and [Apex](https://github.com/apex/apex).

## changes in this fork (diodechain)

1. Added the update.FindZip() func that searches for a '.zip' file instead of '.tar' like the update.FindTarball() func
2. Changed github.latestRelease implementation to compare version strings with dots and dashes numerically. Supported are 'v1.2.3' 'v1.2.3-22' and similiar. Examples:

    - 'v1.2.3-22' > 'v1.2.3'
    - 'v1.2.4' > 'v1.2.3'
    - 'v2' > 'v1.2.3'
    - 'v2' == '2'
    - 'v2.0' == 'v2'
    - 'v2.0.0.0.0' == 'v2'

---

[![GoDoc](https://godoc.org/github.com/diodechain/go-update?status.svg)](https://godoc.org/github.com/diodechain/go-update)
![](https://img.shields.io/badge/license-MIT-blue.svg)
![](https://img.shields.io/badge/status-stable-green.svg)

<a href="https://apex.sh"><img src="http://tjholowaychuk.com:6000/svg/sponsor"></a>
