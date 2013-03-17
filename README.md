Create an account at http://openshift.redhat.com/

Visit https://openshift.redhat.com/community/get-started for help on installing the application management tools. Windows, Mac OS X, RHEL, Ubuntu, Debian and Fedora are covered

Create a PHP 5 application + a PostgreSQL 8 cartridge to the app, and import all the quickstart codes:

	rhc app create <app name> php-5 postgresql-8 --from-code=git://github.com/who-me/ttrss-fast-deployment.git

After this, you need to add cron (for some reason, it errors out if I try to cram it in the above command line):

	rhc cartridge add cron-1.4 -a <app name>

You can now checkout your RSS application at:

	http://<app name>-<your namespace>.rhcloud.com

This app can be shared by multiple users. The default user credential is "admin"/"password".
