MiniMagick integration for Jekyll
=================================

This gem allows you to easily use MiniMagick to crop and resize images in your
Jekyll project, according to a preset defined in your config file.

Basic Setup
-----------
Install the gem:

	add mini_magick.rb to your _plugins directory

Define presets in your _config.yml file, like this:

	# _config.yml
	mini_magick:
		thumbnail:
			source: img/photos/original
			destination: img/photos/thumbnail
			resize: "100x100"
		medium:
			source: img/photos/original
			destination: img/photos/medium
			resize: "600x400"

This configuration will create a 100x100 thumbnail for each image in 
_img/photos/original_ and put it in _\_site/img/photos/thumbnail_ and a 600x400
image in _\_site/img/photos/medium_.

**NOTE**

  Destination is relative to the source directory (the directory your config.yml sits in, by default).