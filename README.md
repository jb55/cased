
# cased

  Track string casing at the type level

## Motivation

  Why? Peace of mind. If you're algorithm is expecting strings with a specific
  case, you might as well enforce it at the type level.

  Knowing the case of a string can be useful to prevent redundant `toUpper` and
  `toLower` applications. If your algorithm is expecting a lower case string,
  you might as well ask for one instead of doing it yourself.

## Installation

    $ cabal install cased

## Example

```hs
import Data.Cased (upperCased, lowerCased, mixedCase)

myName :: Cased Mixed String
myName :: mixedCased "William Casarin"

upperName :: Cased Upper String
upperName = upperCased myName

-- repeated upper/lower casing is a compile error:
doubleUpper = upperCased upperName
--
--    Couldn't match type ‘Yes’ with ‘No’
--    Expected type: No
--      Actual type: IsUpperCased Upper
--
```

## License

  The MIT License (MIT)

  Copyright (c) 2014 William Casarin

  Permission is hereby granted, free of charge, to any person obtaining a copy
  of this software and associated documentation files (the "Software"), to deal
  in the Software without restriction, including without limitation the rights
  to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
  copies of the Software, and to permit persons to whom the Software is
  furnished to do so, subject to the following conditions:

  The above copyright notice and this permission notice shall be included in
  all copies or substantial portions of the Software.

  THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
  IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
  FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
  AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
  LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
  OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
  THE SOFTWARE.
