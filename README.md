# go-month

Simple library to get name of month (full or short form) or number of month in Indonesia.

## Installation

Download and install library:
```go
go get github.com/intaen/go-time
```

## Import
Import in your code
```go
import "github.com/intaen/go-month"
```

## Example
```go
package main

import (
	"fmt"

	"github.com/intaen/go-month"
)

func main() {
    // Example to get date with name of month
    data := "Andi akan pergi ke Amerika pada 2021-09-01"
	conv := strings.Split(data, " ")
	month := inamonth.ConvertDate(conv[6])

	var dt []string
	dt = append(dt, conv[0], conv[1], conv[2], conv[3], conv[4], conv[5], month)
	fmt.Println(strings.Join(dt, " "))
	// Result: Andi akan pergi ke Amerika pada 1 September 2021

	// Example to number of month
    data := inamonth.April
	fmt.Println(int(data))
	// Result: 4
}
```
