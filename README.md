# Contributing to ownCloud.org website

Please take a moment to review this document in order to make the contribution
process easy and effective for everyone involved.    
https://doc.ownCloud.org is not maintained here, but in https://github.com/owncloud/documentation

## Setup of a local development environment

1. Install Wordpress >= 3.8.1
  * Must be in the document root of the webserver (otherwise images won't load :( )
  * Enter what you like for site title, admin user and password, none of this is stored in git
2. Setup the repository
  1. Clone the www repo in a folder of your choice
    * `git clone git@github.com:owncloud/owncloud.org owncloudorgnew`
  2. In the wordpress installation in the wp-content/themes folder, create a link to the folder you just cloned our www repo in under the name 'owncloudorgnew'
3. Activate the theme in Appearance > Themes
4. Import the website content.xml file
  * First install the Wordpress Import Plugin (via Tools > Import > Wordpress Import > Install Plugin)
  * Select the content.xml file from the www repo and click upload
  * Select Import
5. Copy over config.php.sample to config.php and adjust settings as necessary (defaults will work just fine for local environments)
6. In Settings > Reading assign a static front page of 'homepage'

## Development Process

* Fork the www repository
* Setup your local development environment using the instructions above, changing the remote origin url
* Submit a pull request to master, on github once the feature/bugfix is complete (this is so we can test it on the staging server)
* After review (usually following one or two thumbs up), a developer will permit the merge into master
* Code will be pulled onto staging.owncloud.org for testing (deployment there is automatic)
* Once the test looks good, staging will be cloned over to www.owncloud.org - this is handled by @jospoortvliet or the ownCloud, Inc. sysadmins including @danimo 

### Notes

* Please don't commit straight into the master or live branches, these branches should remain as stable as possible, and changes should be discussed amongst the community.
