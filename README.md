# Magento 2 Image Optimizer

This Magento 2 module is a wrapper based on the package [Spatie Image optimizer](https://github.com/spatie/image-optimizer).

## Installation
- `composer require shinetech/magento2-image-optimizer`
- `bin/magento module:enable JustBetter_ImageOptimizer`
- `bin/magento setup:upgrade && bin/magento setup:static-content:deploy`

### Optimize all images in console
- Run `bin/magento justbetter:imageoptimizer:optimizeall` to resize all images in the media folder.
- Additional parameters (will overwrite any option in the magento config):
    - `--jpg_compression="85"`
    - `--jpg_strip_all="1"`
    - `--jpg_all_progressive="0"`
    - `--png_quality_min_max="10-15"`
    - `--png_interlace="0"`
    - `--png_optimization_level="8"`

### Optimization tools

The package will use these optimizers if they are present on your system:

- [JpegOptim](http://freecode.com/projects/jpegoptim)
- [Optipng](http://optipng.sourceforge.net/)
- [Pngquant 2](https://pngquant.org/)
- [SVGO](https://github.com/svg/svgo)
- [Gifsicle](http://www.lcdf.org/gifsicle/)

Here's how to install all the optimizers on Ubuntu:

```bash
sudo apt-get install jpegoptim
sudo apt-get install optipng
sudo apt-get install pngquant
sudo npm install -g svgo
sudo apt-get install gifsicle
```

And here's how to install the binaries on MacOS (using [Homebrew](https://brew.sh/)):

```bash
brew install jpegoptim
brew install optipng
brew install pngquant
brew install svgo
brew install gifsicle
```

## Configuration
- Options for the module are defined in the backend under Stores > Configuration > JustBetter > Image optimizer configuration.
- Possible options:
    - Log the compression in the system.log
    - Change compression of jpg files
    - Change compression of png files

## Compatibility
The module is tested on magento version 2.2.x with Spatie image optimizer version 1.0.x

## Ideas, bugs or suggestions?
Please create a [issue](https://github.com/justbetter/magento2-image-optimizer/issues) or a [pull request](https://github.com/justbetter/magento2-image-optimizer/pulls).

## Todo
- ~~Configurable options for compression~~
- ~~Compress all library images in console command~~

## About us
We’re a innovative development agency from The Netherlands building awesome websites, webshops and web applications with Laravel and Magento. Check out our website [justbetter.nl](https://justbetter.nl) and our [open source projects](https://github.com/justbetter).

## License
[MIT](LICENSE)

---

<a href="https://justbetter.nl" title="JustBetter"><img src="https://raw.githubusercontent.com/justbetter/art/master/justbetter-logo.png" width="200px" alt="JustBetter logo"></a>
