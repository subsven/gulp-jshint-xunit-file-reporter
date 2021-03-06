[![Build Status](https://travis-ci.org/spenceralger/gulp-jshint-xunit-file-reporter.svg?branch=master)](https://travis-ci.org/spenceralger/gulp-jshint-xunit-file-reporter)

## Information

<table>
<tr>
<td>Package</td><td>gulp-jshint-xunit-file-reporter</td>
</tr>
<tr>
<td>Description</td>
<td>simple reporter for gulp-jshint. writes output to a xunit file.</td>
</tr>
<tr>
<td>Node Version</td>
<td>>= 0.3</td>
</tr>
</table>

## Install

    npm install gulp-jshint-xunit-file-reporter --save-dev

## Usage

```javascript
var gulp = require('gulp');
var jshint = require('gulp-jshint');

gulp.task('lint', function() {
  return gulp.src('./lib/*.js')
    .pipe(jshint())
    .pipe(jshint.reporter('gulp-jshint-xunit-file-reporter', {
      filename: __dirname + '/jshint-output'
    }));
});
```

## Options

Plugin options:

Type: `filename`
Default: `"jshint-output"`

The filename prefix to write output from jshint.
This filename is automatically appended with a
number incrementing for the individual output
files and the '.xml' suffix.

## LICENSE

--
The gulp-jshint-xunit-file-reporter is based on
xjamundx/jshint-junit-reporter and spenceralger/gulp-jshint-file-reporter

Copyright 2014 Sven Paulus

--
`xjamundx/jshint-junit-reporter`

Copyright 2012 Derek Prior

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

--
`spenceralger/gulp-jshint-file-reporter`

The MIT License (MIT)

Copyright (c) 2014 Spencer Alger

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
