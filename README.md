# Training FontCustom
Create icon fonts using FontCustom

## Font Custom requirements and installation
Requires:
* Homebrew (Mac)
* Ruby 1.9.3+
* WOFF2
* FontForge build

## Installation on Mac and Linux:
### On Mac
```sh
brew tap bramstein/webfonttools
brew update
brew install woff2

brew install fontforge --with-python
brew install eot-utils
gem install fontcustom
```

### On Linux
```sh
sudo apt-get install zlib1g-dev fontforge build-essential rubygems
git clone https://github.com/bramstein/sfnt2woff-zopfli.git sfnt2woff-zopfli && cd sfnt2woff-zopfli && make && sudo mv sfnt2woff-zopfli /usr/local/bin/sfnt2woff
git clone --recursive https://github.com/google/woff2.git && cd woff2 && make clean all && sudo mv woff2_compress /usr/local/bin/ && sudo mv woff2_decompress /usr/local/bin/
sudo gem install fontcustom
```
More details at [https://github.com/FontCustom/fontcustom](https://github.com/FontCustom/fontcustom)

## Generate the font
1. Running `fontcustom compile` will generate font files in build folder.
2. Open the `build/fonticons.html` in your browser and check everything's good with the new generated font.

-------------------------------

## Update font with two new icons
1. Go to [https://vectr.com/](https://vectr.com/) and create two new svg icons (100x100 px, #000000, no outlines)
2. Save them in `assets/icons`
3. Compile font
4. Test font
