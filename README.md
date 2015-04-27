# Uno - A theme for [Ghost]
### Attribution Notice
This is a derivative work, forked from [the original Uno theme] by [Dale Anthony] and licensed under [Creative Commons Attribution 4.0 International]. It has been heavily modified for use by a Rubyist.

I would like to personally thank Dale for the use of his excellent material!

## Demo
View this theme in action on my technical blog [ComputeThis](http://blog.sensiblesolutions.me)

## Features

- **Cover page** - The landing page for Uno is a full screen 'cover' featuring your avatar, blog title, mini-bio and cover image.
- **Responsive** - Uno looks great on all devices, even those weird phablets that nobody buys.
- **5 color options** - Uno includes 5 different color options for you to chose from.
- **Disqus integration** - The easiest way to let people comment on your blog.
- **Foundation icons** - Uno contains the quality [Foundation icon font by Zurb].
- **No-JS fallback** - While JS is widely used, some themes and websites don't provide fallback for when no JS is available (I'm looking at you [Squarespace](http://blog.squarespace.com/)). If for some weird reason a visitor has JS disabled your blog will still be useable.
- **Built with SASS, using BEM**

## Development

In order to develop or make changes to the theme you will need to have the sass compiler and bourbon both installed.  If you are running a Ghost environment locally then you should already have these installed as those are required to run Ghost.

To check installation run the following commands from a terminal and you should see the `> cli output` but your version numbers may vary.

** SASS **
```bash

sass -v
> Sass 3.3.4 (Maptastic Maple)
```
If for some reason SASS isn't installed follow the instructions from the [Sass install page](http://sass-lang.com/install)

** Bourbon **
```bash

bourbon help
> Bourbon 3.1.8
```
If Bourbon isn't installed follow the installation instructions on the [Bourbon website](http://bourbon.io)

Once installation is verified we will need to go mount the bourbon mixins into the `scss` folder.

From the project root run `bourbon install` with the correct path
```bash
bourbon install --path assets/scss
> bourbon files installed to assets/scss/bourbon/
```

Now that we have the bourbon mixins inside of the `scss` src folder we can now use the sass cli command to watch the scss files for changes and recompile them.

```bash
sass --watch assets/scss:assets/css
>>>> Sass is watching for changes. Press Ctrl-C to stop.
```

** MacOSX Maverick **

Some people may receive this error when trying to run the `sass --watch` command

```bash
> LoadError: cannot load such file -- rb-fsevent
  Use --trace for backtrace.
```

This is a known issue with the [Sass on MaxOS Maverick](http://stackoverflow.com/questions/22413834/getting-error-when-using-command-line-for-sass-to-watch-files) as indicated install the `rb-fsevent` gem

```bash
gem install rb-fsevent
```

## Deployment
To use this theme on Ghost's official hosting platform, or otherwise deploy, you'll need to run the following commands from the project root:

```bash
bourbon install --path assets/scss
slimrb source/partials/social.slim partials/social.hbs
```


[Ghost]: https://ghost.org/
[the original Uno theme]: https://github.com/daleanthony/uno
[Dale Anthony]: dale@daleanthony.com
[Creative Commons Attribution 4.0 International]: http://creativecommons.org/licenses/by/4.0/
[Foundation icon font by Zurb]: http://zurb.com/playground/foundation-icon-fonts-3
[Foundation icon website]: http://zurb.com/playground/foundation-icon-fonts-3