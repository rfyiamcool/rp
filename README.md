# rp

rp is reverse proxy in golang.

```
package main

import (
	"github.com/gin-gonic/gin"
	"github.com/rfyiamcol/ginproxy"
)

func main() {
	router := gin.Default()
	g, _ := ginproxy.NewProxy("http://127.0.0.1:10001")
	router.Any("/", g.Handler)
	router.Run(":8080")
}
```
