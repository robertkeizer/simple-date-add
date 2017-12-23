## Overview

Sometimes you want to transform JSON data. This package parses data from standard in and creates a new object with `year`, `month`, `dateOfMonth`, `dayOfWeek`, `hour`, `minute`, and `seconds` fields.

The property of the incoming objects that contains the date field is specified with `-d`.

The expanded output object containing the above mentioned fields is in the form of `datefield + _expanded`. Assuming you have a date object named `date`, the added object would be `date_expanded`.

## Installation

```
npm install -g simple-date-add
```

## Usage

```
  Usage: simple-date-add [options]


  Options:

    -V, --version                output the version number
    -d, --datefield [datefield]  The property that contains the date object.
    -i, --ignore                 Ignore inputs that don't contain datefield; ( Don't die )
    -h, --help                   output usage information
```

## Examples

**Example**: Take the output of [ifstat-json](https://github.com/robertkeizer/ifstat-json) and expand the output.
```
$ ifstat-json | simple-date-add -d date
```
