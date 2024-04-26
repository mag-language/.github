![mag banner](https://world-of-music.at/downloads/bird-banner.png)

# Introduction

Mag is an optionally typed programming language with patterns, classes and multiple dispatch.

A simple Fibonacci function could look like this in Mag:

```python
def fib(0) 0
def fib(1) 1
def fib(n Int) fib(n - 2) + fib(n - 1)
```

You can also implement this using a `match` statement:

```python
def fib(n Int)
  match n
    case 0 then 0
    case 1 then 1
    case n then fib(n - 2) + fib(n - 1)
  end
end
```

As you can see, there are three method definitions with different arguments which share the same name. When the method named `fib` is called, the appropriate method body is chosen at runtime so that `fib(0)` returns `0`, `fib(1)` returns `1` and `fib(n)` returns the Fibonacci number for any other input by calling itself recursively and calculating the result.

## Credits

Mag is based on the Magpie language by [Robert Nystrom](http://stuffwithstuff.com/), who is a language engineer at Google with [a blog and a lot of amazing ideas](http://journal.stuffwithstuff.com/category/magpie/). His various blog posts are what started and inspired this project, and I plan on continuing his legacy even if the original codebase ceases further development.

However, since there are a few syntactical differences to the original Magpie language, the two languages are *source-incompatible* and thus have different names. In particular, Bob's implementation substitutes the dot commonly used for calling methods on objects with a space (usually a meaningless character), which I find rather unintuitive, especially for new programmers.
