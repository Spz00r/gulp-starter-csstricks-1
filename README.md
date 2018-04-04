Installation
============

Prerequisites
-------------

### Unix
1. npm
2. bower (npm install -g bower)

### Windows
1. git for windows (including gitBash) https://github.com/git-for-windows/git/releases/tag/v2.12.2.windows.2
2. npm (from node.js package) https://nodejs.org/en/download/
3. bower (npm install -g bower)

Install
-------
1. Install nodejs. https://nodejs.org/en/
2. Check npm (node package manager) is installed via command prompt:
```bash
$ npm
```
3. Install gulp:
```bash
$ npm install gulp --global
```
4. In relevant project folder, create 'gulpfile.js':
```bash
    // build flow that copies MyNiceProgram.exe to another
    // directory (with forced folder creation and overwrite)
    
    var gulp = require('gulp');
    var exefile = 'some/bin/path/MyNiceProgram.exe';
    
    gulp.task('build', function(){
        gulp.src(exefile).pipe(gulp.dest('../../Binaries/'));
    });
    
    gulp.task('default', ['build'], function(){
        gulp.watch(exefile, ['build']);
    });
```

### clone repository

```bash
$ git clone ssh://git@LINK-TO-GIT/NAME-GIT.git
```

You may also clone this using https:

```bash
$ git clone https://<your_bitbucket_account>@bitbucket.org/LINK-TO-GIT/NAME-GIT.git
```

# switch directory to the new
```bash
$ cd NEW-DIRECTORY/
```

### switch branch to develop
```bash
$ git checkout develop
```

### install npm libraries

```bash
$ npm install
```

### install bower libraries

```bash
$ bower install
```

### Run Gulp:

```bash
$ gulp
```

This will start local server on http://localhost:3000/ with file watcher and all required tools to handle *.scss changes/build
