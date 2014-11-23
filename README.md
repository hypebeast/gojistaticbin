# goji-staticbin

goji-staticbin is a middleware for [https://github.com/zenazn/goji](Goji) that serves static files from a [https://github.com/jteeuwen/go-bindata](go-bindata)generated asset file.

# Usage

```go
package main

import (
    "github.com/hypebeast/gojistaticbin"
    "github.com/zenazn/goji"
)

func main() {
    goji.Use(gojistaticbin.Staticbin("static", Asset, gojistaticbin.Options{
        SkipLogging: false,
        IndexFile:   "index.html",
    }))

    goji.Serve()
}

```

See the `examples` folder for an example application that uses goji-staticbin.

