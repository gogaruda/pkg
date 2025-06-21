# Personal PKG

## Install
```
go get github.com/gogaruda/pkg@v1.0.0
```

## Middleware
### 1. CORS Middleware
```go
package main

import (
	"github.com/gin-gonic/gin"
	"github.com/gogaruda/pkg/middleware"
	"os"
	"strings"
)

func getAllowedOrigins() []string {
	origins := os.Getenv("ALLOWED_ORIGINS")
	if origins == "" {
		return []string{"http://localhost:3000"}
	}
	return strings.Split(origins, ",")
}

func main() {
	r := gin.Default()
	r.Use(middleware.CORSMiddleware(getAllowedOrigins()))
}
```

## APPERROR

## Database
### 1. ACID(Atomicity, Consistency, Isolation, and Durability)
```go

```