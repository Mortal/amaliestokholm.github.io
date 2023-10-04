# Personal website.
### How to set-up
```
sudo apt install ruby-bundler
bundle install --path vendor/bundle
```

### How to build locally:

```
bundle exec jekyll serve
```

# Overview of structure

## Things necessary for the webpage
- `_layouts`: contains the actual set-up of webpage. In `default.html`, you find what sections are included where and in `blog.html` you find the set-up for the blog. This uses the template in `tpw.html`.
- `_includes`: Home for all the html that are the building blocks of the main web site. This includes the `about` section, `outreach`, `research`, `contact`, the link to the `blog` and the `header` and `footer`.
- `img`: contains images and icons for website.
- `css`: contains the css files. It contains both the normal file and the minimised files (min.css) for some reason - maybe it should just be one or the other..
- `fonts`: contains fonts and icons.
- `js`: contains javascript for `bootstrap` (main framework), `particles.js` (for the moving "stars") `jquery` and `instafeed` (which is kinda broken now).
- `rsc`: contains other files to be used on the website. Currently just a cv.
- `scss`: scss files for Ruby to use in the jekyll set-up. Style sheets for the visual elements of the webpage (buttons, themes etc.)
- `vendor`: packages for the website, e.g. `jekyll` and `font-awesome`.
- (not in git) `node_modules`: blocks of code for external applications. Mostly used for node.js

## Things necessary for blog
- `_posts`: contains the markdown files for the blogposts. They follow a specific naming convention, i.e. `yyyy-mm-dd-keyword.markdown`. If you do not want a blog post to be public yet, you can either omit pushing it to the git directory or set a date in the future (?).
- `images`: contains images for blog posts. It is sorted into subfolders relating to the relavant blogpost.
- Files in `_includes` and in `_layouts`.

Floating on top:
- `Gemfile`: Essential jekyll set-up
- `Gemfile.lock`: Essential list of modules for Jekyll
- `gulpfile.js`: Essential set-up for ruby and third party libraries.
- `.gitignore`: file to specify what files to hide from git. This could be `secrets.txt`.
- (not in git) `secrets.txt`: txt file containing a single line with my `ADS_API_TOKEN`.
- `_config.yml`: simple config file for jekyll. Contains settings for webpage and for buttons and counter.
- `adsexport.py`: python script that gets my most recent publications from my ADS library.
- other files starting with `adsexport`: can be deleted. Temporary files for ads query.
- `CNAME`: txt file containing my alias (a.strova.dk) for this webpage.
- `LICENSE`: MIT License file

