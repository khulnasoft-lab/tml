# tml - Terminal Markup Language

[![Build Status](https://travis-ci.org/khulnasoft-lab/tml.svg "Travis CI status")](https://travis-ci.org/khulnasoft-lab/tml)
[![GoDoc](https://godoc.org/github.com/khulnasoft-lab/tml?status.svg)](https://godoc.org/github.com/khulnasoft-lab/tml)

A Go module (and standalone binary) to make the output of coloured/formatted text in the terminal easier and more readable.

You can use it in your Go programs, and bash etc. too.

![Example screenshot](example.png)

## Usage in Go

The output of coloured/formatted text is easy using the following syntax:

```go
package main

import "github.com/khulnasoft-lab/tml"

func main() {
    tml.Printf("<red>this text is <bold>red</bold></red> and the following is <green>%s</green>\n", "not red")
}
```

## Usage in Bash

First, install tml:

Install Go and run the following command.

```
# For Go 1.16+
# Make sure that `$GOPATH/bin` is in your `$PATH`, because that's where this gets installed

go install github.com/khulnasoft-lab/tml/tml@latest

# For Go <1.16

go get -u github.com/khulnasoft-lab/tml/tml
```

Then you can simply pipe text containing tags to tml:

```bash
#!/bin/bash

echo "<red>this text is <bold>red</bold></red> and the following is <green>not red</green>" | tml
```

## Format

Each tag is enclosed in angle brackets, much like HTML.

You can nest tags as deeply as you like.

It's not required to close tags you've opened, though it can make for easier reading.

### Available Tags

#### Foreground Colours

- `<red>`
- `<green>`
- `<yellow>`
- `<blue>`
- `<magenta>`
- `<cyan>`
- `<lightgrey>`
- `<darkgrey>`
- `<black>`
- `<white>`
- `<lightred>`
- `<lightgreen>`
- `<lightyellow>`
- `<lightblue>`
- `<lightmagenta>`
- `<lightcyan>`

#### Background Colours

- `<bg-red>`
- `<bg-green>`
- `<bg-yellow>`
- `<bg-blue>`
- `<bg-magenta>`
- `<bg-cyan>`
- `<bg-lightgrey>`
- `<bg-darkgrey>`
- `<bg-black>`
- `<bg-white>`
- `<bg-lightred>`
- `<bg-lightgreen>`
- `<bg-lightyellow>`
- `<bg-lightblue>`
- `<bg-lightmagenta>`
- `<bg-lightcyan>`

#### Attributes

- `<bold>`
- `<dim>`
- `<italic>`
- `<underline>`
- `<blink>`
- `<reverse>`
- `<hidden>`
