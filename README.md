# Personal Website - [antoniyaat.com](https://antoniyaat.com)


>  Personal website including full setup for **[Jekyll](https://jekyllrb.com/)**, **[GulpJS](https://github.com/gulpjs/gulp)** & **[SASS](https://sass-lang.com/)**.

## System Preparation

To use this starter project, you'll need the following things installed on your machine.

1. [Jekyll](https://jekyllrb.com/) - ```$ gem install jekyll```
2. [NodeJS](https://nodejs.org/en/) - use the installer
3. [GulpJS](https://github.com/gulpjs/gulp) - ```$ npm install -g gulp ```

## Local Installation
1. Clone this repo, or download it into a directory of your choice
2. Inside the directory, run ```npm install```

## Usage 
This will give you file watching, browser synchronisation, auto-rebuild, CSS injecting etc etc.

```$ gulp```

As this is just a Jekyll project, you can use any of the commands listed in their docs


```$ jekyll```

## Deploy with Gulp
You can easily deploy your site build to a [gh-pages](https://github.com/shinnn/gulp-gh-pages) branch. First, follow the instructions at **gulp-gh-pages** to get your branch prepared for the deployment and to install the module. Then, in gulpfile.js you'll want to include something like the code below. gulp.src() needs to be the path to your final site folder, which by default will be _site. If you change the destination in your _config.yml file, be sure to reflect that in your gulpfile.

```
var deploy = require("gulp-gh-pages");

gulp.task("deploy", ["jekyll-build"], function () {
    return gulp.src("./_site/**/*")
        .pipe(deploy());
});
```
