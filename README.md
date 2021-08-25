# SRFI nnn: Macroexpand

by Firstname Lastname, Another Person, Third Person

## Status

Early Draft

## Abstract

This SRFI displays the Scheme code that results from expanding a macro, without actually evaluating that code --
an essential tool for debugging macros.

## Issues

## Rationale

### Survey of prior art

Common Lisp has [standard `macroexpand` and `macroexpand-1` functions](http://www.lispworks.com/documentation/HyperSpec/Body/f_mexp_.htm).

https://doc.scheme.org/surveys/MacroExpand/

## Specification

`(macroexpanded? form) => boolean`

`(macroexpand form [environment]) => expansion, expanded?`

`(macroexpand-1 form [environment]) => expansion, expanded?`

`(macroexpand-n form [environment [n]]) => expansion, expanded?`

## Examples

`(macroexpand '(cond (a 1) (else 2)))`

## Implementation

The implementation of this SRFI depends deeply on the macro systems available in each Scheme implementation, and how those macro systems are implemented in detail.

## Acknowledgements

Common Lisp, #chicken IRC

## References

## Copyright

Copyright (C) Firstname Lastname (20XY).

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
