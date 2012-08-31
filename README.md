### ios-resize
ios-resize a command line tool used to automatically resize PNG images from retina resolutions to non-retina resolutions. Saving out two versions of the same image in PhotoShop is an annoying chore that makes developers less productive so a computer should do it instead!

ios-resize will work for PNG files using Apple's naming convention (@2x) as well as the cocos2d framework naming conventions (-hd and -ipadhd). ios-resize defaults to resizing PNG files in a single directory but can be flagged to recursively look through all children directories as well. Please refer to the Usage and Installation sections for more information.

Image resizing is done using PHP's image processing library.

ios-resize was developed for the Mac OS X 10.8 operating system since most iOS development happens on a Mac and PHP comes preinstalled on every Mac.

### Usage:

In the Terminal, run:
 
`ios-resize *`

This will resize all images in the current folder.

`ios-resize file@2x.png file2@2x.png`

This will resize the two images specified.

`ios-resize * -d`

This will resize all images in the current directory as well as all children directory recursively.
 
### Installation
 
Make sure your path to PHP is located at /usr/bin/php otherwise edit the first line to point to PHP. Save the file if you changed the path to PHP.

In the Terminal, go to where the ios-resize file is and run:

`chmod 777 ios-resize`

Then copy the file to your /usr/bin directory by running:

`cp ./ios-resize /usr/bin/ios-resize`

You may get a permission error so instead do:

`sudo cp ./ios-resize /usr/bin/ios-resize`

And enter your password when prompted. This assumes your user account has proper permissions to write to the /usr/bin folder.
 
### Alternate Installation

Make sure your path to PHP is located at /usr/bin/php otherwise edit the first line to point to PHP. Save the file if you changed the path to PHP. And you're done. The only difference is that usage will look like this instead:

`php ios-resize * -d`

ios-resize is released under the MIT License.

### Authors and Contributors
ios-resize is built by Tommy Leung on top of work by Jonathan Ellis on his [blog](http://jona.than.biz/blog/generating-non-retina-images-automatically-for-ios/). Features not found in original implementation include:

* cocos2d format support
* recursively directory search
* usage instructions in command line
* comments on how it works (if you care)

I do not personally know Jonathan Ellis, I just found his code on Google and thought it was quite useful so I extended it.

### Support or Contact
There's really no support but you tweet me [@iamsupertommy](http://twitter.com/iamsupertommy) or find me on Github @supertommy and I'll see if I can help you.