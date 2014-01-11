# clean-greader

clean-greader is a tiny tiny rss (1.8+) theme based on the latest Google Reader and inspired by other Google Services.
As of 2013/08/29 the theme is build from scratch to be independent from changes to the tt-rss default.css.

## Preview
![](img/preview.png)

## Installation
### Using Git
Assuming, that your tt-rss instance is located at /usr/share/tt-rss:
```bash
cd /usr/share/tt-rss/themes
git clone https://github.com/naeramarth7/clean-greader
ln -s ./clean-greader/clean-greader.css ./clean-greader.css
```

### Manual
1. Download the package using the "Download ZIP" button on the right
2. Copy the clean-greader-master folder into you tt-rss/themes folder (e. g. /usr/share/tt-rss/themes) and rename it to clean-greader
3. Copy the clean-greader.css file from the clean-greader folder into you themes root folder (e. g. /usr/share/tt-rss/themes)

## Update
### Using git
Assuming, that your tt-rss instance is located at /usr/share/tt-rss:
```bash
cd /usr/share/tt-rss/themes/clean-greader
git pull
```

### Manual
Same as Installation - just overwrite the files.

## Maintenance
As of the "build from scratch" update, the theme is completely written using [SASS/SCSS](http://sass-lang.com/).
maA tutorial on [Devloping With Sass and Chrome DevTools](http://net.tutsplus.com/tutorials/html-css-techniques/developing-with-sass-and-chrome-devtools/) can be found on net.tutsplus.com.

By running the `css/convert-main.scss.sh`* or `css/watch-main.scss.sh`* script any change to any contained `.scss` file will automatically be translated into  the `main.css`.

---

*sass needs to be installed on your the server.
```
gem install sass --pre
```

## Support
The clean-greader theme is build on Google Chrome (29 beta) using Linux Mint 15 and tested on Google Chrome (29 beta) as well as Mozilla Firefox (23).
These are the only official support browsers, so there will be no guarantee for the usability on other browsers except of those.

## FAQ
#### My images from image feed xy are too small! Why's that?
The first image in an article is displayed with a max resolution of 128x128 to provide some sort of preview. I decidet to implement this, since I have a lot of feed just displaying a very large image before any content. Meh.

However, there's a feature to override this setting for any domain. The configuration is stored within the `css/config/_fullsizeimages.scss` file. Take a look at source of the images in your articles and add one filter per line for each domain you want to disable the preview feature.

Don't forget to run the `css/convert-main.scss.sh` file after making any changes to scss files.

## Tiny Tiny RSS Settings
| Setting                                          | Value      |
|:------------------------------------------------ |:----------:|
| `Combined feed display`                          | `enabled`  |
| `Automatically expand articles in combined mode` | `disabled` |
| `Show content preview in headlines list`         | `disabled` |

## Screenshots
### Main Page
![](img/preview_02.png)

### Main Settings
![](img/preview_03.png)

### Feed Settings
![](img/preview_04.png)

---

[![Flattr this git repo](http://api.flattr.com/button/flattr-badge-large.png)](https://flattr.com/submit/auto?user_id=naeramarth7&url=https://github.com/naeramarth7/clean-greader&title=clean-greader&language=&tags=github&category=software)
