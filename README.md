# Wordpress Kitematic Project #

This repo is a fork from the official wordpress docker repo, modified to explicity define a volume to make the upload.ini conf file accessible from kitematic.

Create an uploads.ini, defining the acceptable upload configurations. An example is as follows:

	file_uploads = On
	memory_limit = 2M
	upload_max_filesize = 2M
	post_max_size = 2M
	max_execution_time = 600

Map upload.ini file to the appropriate directory, i.e.

	volumes: uploads.ini:/usr/local/etc/php/conf.d/uploads.ini

### Credits
val creator = _profile( "**[Mark Bonano](http://www.linkedin.com/pub/mark-bonano/6/23/92a)**" ).withRamblingsAt( "[letitscale.com](http://letitscale.com)" )_