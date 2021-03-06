Tumblr Photo Fetch
==============

A simple script to download pictures from the Tumblr Photo Blogs (works great with [New Old Stock](http://nos.twnsnd.co/)).
Runs in the background with launchd on OS X, could be adapted on other systems.

Setup
-----

0. Download this repo in ZIP file and extract it wherever you want on your system.
1. Open Terminal, `cd` in the folder containing the repo files.
2. Execute: `mkdir -p "~/Pictures/New Old Stock"`
3. Execute: `ln -sfv "$(pwd)/newoldstock-dl.php" /usr/local/bin`
4. Execute: `ln -sfv "$(pwd)/com.mcdado.newoldstock.plist" ~/Library/LaunchAgents/`
5. Execute: `launchctl load ~/Library/LaunchAgents/com.mcdado.newoldstock.plist`
6. Setup your preferred OS X Screensaver to look into `"~/Pictures/New Old Stock"`

If you want to point to another Tumblr blog, edit the file `newoldstock-dl.php` and change the domain of `http://nos.twnsnd.co/api/read` to any other blog.

Notes
-----

* I assume you are using homebrew's php. If you're not, edit the file `unsplash-dl.php` at the first line with `#!/usr/bin/php`;
* The script requires [pecl\_http v2](http://pecl.php.net/package/pecl_http). You can install pecl_http with homebrew (php5*-http) or via PECL.
* This is distributed as is. It's quite a hack. Use at your own peril.
