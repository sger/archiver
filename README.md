[![Build Status](https://travis-ci.org/sger/podule.svg?branch=master)](https://travis-ci.org/sger/podule)
[![Coverage Status](https://coveralls.io/repos/github/sger/podule/badge.svg?branch=master)](https://coveralls.io/github/sger/podule?branch=master)

# Go Archiver

Simple Archiving with Golang

```go
package main

import (
	"fmt"

	"github.com/sger/archiver"
)

func main() {

	err := archiver.GetInstance().Archive("src/go", "src/output/files.zip")

    // Throw error if directory don't exists
	if err != nil {
		fmt.Println(err)
	}

	err = archiver.GetInstance().Restore("src/output/files.zip", "src/output/restored")

	if err != nil {
		fmt.Println(err)
	}
}
```

Author
-----

__Spiros Gerokostas__ 

- [![](https://img.shields.io/badge/twitter-sger-brightgreen.svg)](https://twitter.com/sger) 
- :email: spiros.gerokostas@gmail.com

License
-----

Go Archiver is available under the MIT license. See the LICENSE file for more info.

