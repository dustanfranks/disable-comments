==== MODIFIED FOR AFROZAAR ====

Contributor: Dustan Franks, Afrozaar Consulting 
Github repo: https://github.com/dustanfranks/wp-plugin-disable-comments

This is a fork of the Disable comments plugin for Wordpress. (see README details below for original author & plugin information.)

The only difference made in this fork is redirecting comment feed URLS on posts back to the original post itself instead of die(); and displaying a "comments are closed message"

public function filter_query() {
        
        if( is_comment_feed() ) {

            $pageURL = substr( $GLOBALS['path'], 0, strpos($GLOBALS['path'], '/feed') );
            header('Location: ' . $pageURL);
            die();
            
        }
    }

# Disable Comments for WordPress

[![Build Status](https://travis-ci.org/solarissmoke/disable-comments.svg?branch=master)](https://travis-ci.org/solarissmoke/disable-comments)

This is the development respository for the [Disable Comments](https://wordpress.org/plugins/disable-comments/) WordPress plugin. Send pull requests here, download the latest stable version there!

Version and compatibility information can be found in the plugin [readme](https://github.com/solarissmoke/disable-comments/blob/master/readme.txt) file.

License: [GPLv2](https://www.gnu.org/licenses/gpl-2.0.html)

## Must-Use version

A [must-use version](https://github.com/solarissmoke/disable-comments-mu) of the plugin is also available.
