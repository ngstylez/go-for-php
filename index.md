# Go for PHP Developers


# Me

Director of Engineering at Chapter Three
PHP'n since 2003
Golang'n since 2014


# Background
##
"Most interesting thing about Go is that it's not object oriented or procedural or functional, it's its own new exciting thing"
- David Kinzer https://twitter.com/dtkinzer/status/786031866478407681
##
"with Go I was able to pick up programming / CS concepts rather quickly, enjoy the process, and learn a ton of things in the meantime"
- Audrey Lim  https://youtu.be/fZh8uCInEfw
##
"Although Go is quite a small language, it is a very rich and expressive language (as measured in syntactic constructs, concepts, and idioms), so there is a surprising amount to learn."
- Freddy Rangel http://spaces-vs-tabs.com/4-weeks-of-golang-the-good-the-bad-and-the-ugly/
##
"Even if you’re a dynamic language zealot, I bet you’d be shocked how productive you can be with a statically typed language like Go."
- Blake Smith http://blakesmith.me/2012/08/19/why-you-should-learn-to-program-in-go.html
##
"Golang is a very pleasant language to get systems-y things done in. I'm fond of saying that it's not an amazing language, but is an amazing programming tool."
- tptacek https://news.ycombinator.com/item?id=9381093
##
"When launching a new language it is important that the target audience be able to learn it quickly; rooting Go in the C family helps make sure that young programmers, most of whom know Java, JavaScript, and maybe C, should find Go easy to learn."
- Rob Pike https://talks.golang.org/2012/splash.article#TOC_12.

# Hello World
## Download: https://golang.org/doc/install
## untar it in /usr/local
## Tell Shell about Go
`$ export PATH=$PATH:/usr/local/go/bin`

## Tell Go where your code is
`$ export GOPATH=$HOME/work`


## `go fmt`
- Pollution (won't allow unnused things)
- Tabs vs Spaces (WHO CARES)
- One standard to rule them all

## 
```
package main

import "fmt"
import "github.com/4ad/doozer"

func main() {
	fmt.Println("Hello, 世界")
}
```
##
https://4.bp.blogspot.com/-O4jXmTm7WWI/Tyw1As8jt7I/AAAAAAAAI9E/nxxi1T21IH4/s1600/unicode.png


## 
```
...
package main
...
```

## 
```
...
import "fmt"
...
```

## 
```
...
func main() {
	fmt.Println("Hello, 世界")
}
...
```


## `go install`

## `go run`

## `go build`

# declaration plus assignment operator (:=)
 In Go, := is for declaration + assignment, whereas = is only for assignment only.


# CSP

## 
```
// A _goroutine_ is a lightweight thread of execution.

package main

import "fmt"

func f(from string) {
    for i := 0; i < 3; i++ {
        fmt.Println(from, ":", i)
    }
}

func main() {

    // Suppose we have a function call `f(s)`. Here's how
    // we'd call that in the usual way, running it
    // synchronously.
    f("direct")

    // To invoke this function in a goroutine, use
    // `go f(s)`. This new goroutine will execute
    // concurrently with the calling one.
    go f("goroutine")

    // You can also start a goroutine for an anonymous
    // function call.
    go func(msg string) {
        fmt.Println(msg)
    }("going")

    // Our two function calls are running asynchronously in
    // separate goroutines now, so execution falls through
    // to here. This `Scanln` code requires we press a key
    // before the program exits.
    var input string
    fmt.Scanln(&input)
    fmt.Println("done")
}
```


# moar stuff

More thinkgs
- and these things
- and these too

# Credits:
https://github.com/eosrei/rjsmake

# Resources:
https://golang.org/doc/effective_go.html
On Reddit: r/golang and r/learngolang
Todd McLeod - Udemy Course https://www.udemy.com/learn-how-to-code/
https://www.infoq.com/presentations/clojure-core-async
https://golang.org/doc/effective_go.html
hackerrank.com
https://youtu.be/fZh8uCInEfw

#Examples
https://github.com/coreos/etcd
https://github.com/docker
https://github.com/hybridgroup/gobot
