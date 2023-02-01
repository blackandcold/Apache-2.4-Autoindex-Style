ABOUT
-----
A better looking directory listing for Apache. For sure.
Also works with subdirectories.

Be aware that Indexing has to be turned on for your folder, or otherwise you will never see the Apache file index.

I took the original idea and moved it to work with Apache 2.4

Most notable this comment helped figure out why PHP was not parsed when changing header/footer to .php
https://stackoverflow.com/a/41089342


REQUIREMENTS
------------
- PHP
- autoindex
- mime (probably)
- include (maybe)

INSTALL
-------
1. clone repo to somewhere safe on your server (has to be at the www root level or files will not be loaded!)
2. Open up apache httpd.conf and add this line:

		Include <path/to/git-repo/>/autoindex.conf
	
	Make sure autoindex_module is installed and enabled
	
		LoadModule autoindex_module modules/mod_autoindex.so

	If found, **comment out** any reference to httpd-autoindex.conf. We are replacing this.


3. **Open autoindex.conf and edit the path on line 7 and 17.**
4. Restart Apache

CUSTOM THEME
----------------
You can create your own .css file in the css folder and reference it in the header.php file, line 29. 

EXAMPLE
-------
![example](http://i.solidfiles.net/b215662ded.png)


LICENSE
-------

Based on https://github.com/eigan/Apache-Autoindex-Style (see Fork base)

Icons		
		
	All Icons are Copyright © Yusuke Kamiyamane. All rights reserved. Licensed under a Creative Commons Attribution 3.0 license.
	
	http://p.yusukekamiyamane.com/
	http://creativecommons.org/licenses/by/3.0/	
