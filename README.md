# go-plan9-binaries
Download Go binaries for Plan 9. Go is cross-compiled on linux for all supported architectures: amd64, 386 and arm.
The build happens automatically using a GitHub Action when a release tag is pushed.

## Installation

Example installation of go1.16.3 on amd64:
```
cd /amd64
hget https://github.com/fhs/go-plan9-binaries/releases/download/go1.16.3/go-plan9-amd64-bootstrap.tbz > go-plan9-amd64-bootstrap.tbz
tar xf go-plan9-amd64-bootstrap.tbz
rm go-plan9-amd64-bootstrap.tbz
mv go-plan9-amd64-bootstrap go
bind -b /amd64/go/bin /bin
GOROOT=/amd64/go
go version  # should print "go version go1.16.3 plan9/amd64"
```

## See also
* [Go binaries at 9legacy.org](http://9legacy.org/download.html)
