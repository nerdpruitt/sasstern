# sasstern
A small mixin and function library for Sass.

## Why yet another Sass lib?
I like to keep my Sass close to good ol' plain CSS, so I don't typically use a lot of mixins and functions. However, I find myself returning to a few simple things that really speed me up, so here it all is. The majority of this comes from the work I've done over the years with my good friend Jake Fentress as a part of the [Sasspool](https://github.com/guerillalabs/Sasspool) project. I have tweaked it here and there for use in projects at my company and wanted to abstract it into an NPM package for easy reuse across our projects, so here it is.


## Install
`npm install sasstern --save-dev`


## Example Use with Gulp
```
// gulpfile.js
gulp.task('sass', function() {
    return gulp.src('scss/*.scss')
        .pipe(sass({
            outputStyle: 'compressed',
            includePaths: ['node_modules/sasstern/sass']
        }).on('error', sass.logError))
        .pipe(gulp.dest('dist/css'));
});
```

## Settings
After installing, all you need is a [settings file](https://github.com/nerdpruitt/sasstern/blob/master/_settings.scss), and you are ready to go!

```
/* app.scss */
@import "sasstern";
@import "settings";

// @import the rest of your code :D
```
