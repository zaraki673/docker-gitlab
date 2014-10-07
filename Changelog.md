# Changelog

**7.3.2-1**
- fix mysql status check

**7.3.2**
- upgrade to gitlab-ce 7.3.2
- removed internal mysql server
- added support for fetching `DB_NAME`, `DB_USER` and `DB_PASS` from the postgresql linkage
- added support for fetching `DB_NAME`, `DB_USER` and `DB_PASS` from the mysql linkage
- gitlab-shell: upgrade to v.2.0.1
- added GITLAB_GRAVATAR_ENABLED configuration option
- added fig.yml

**7.3.1-3**
- fix mysql command again!

**7.3.1-2**
- fix mysql server status check

**7.3.1-1**
- plug bash vulnerability by switching to dash shell
- automatically run the `gitlab:setup` rake task for new installs

**7.3.1**
- upgrade to gitlab-ce 7.3.1

**7.3.0**
- upgrade to gitlab-ce 7.3.0
- added GITLAB_WEBHOOK_TIMEOUT configuration option
- upgrade to gitlab-shell 2.0.0
- removed internal redis server
- shutdown the container gracefully

**7.2.2**
- upgrade to gitlab-ce 7.2.2
- added GITLAB_HTTPS_HSTS_ENABLED configuration option (advanced config)
- added GITLAB_HTTPS_HSTS_MAXAGE configuration option (advanced config)
- upgrade to gitlab-shell 1.9.8
- purge development packages after install. shaves off ~300MB from the image.
- rebase image on sameersbn/debian:jessie.20140918 base image
- added GITLAB_SSH_HOST configuration option
- added GITLAB_USERNAME_CHANGE configuration option

**7.2.1-1**
- removed the GITLAB_HTTPS_ONLY configuration option
- added NGINX_X_FORWARDED_PROTO configuration option
- optimization: talk directly to the unicorn worker from gitlab-shell

**7.2.1**
- upgrade to gitlab-ce 7.2.1
- added new SMTP_ENABLED configuration option.

**7.2.0-1**
- fix nginx static route handling when GITLAB_RELATIVE_URL_ROOT is used.
- fix relative root access without the trailing '/' character
- added seperate server block for http config in gitlab.https.permissive. Fixes #127
- added OAUTH_GOOGLE_RESTRICT_DOMAIN config option.

**7.2.0**
- upgrade to gitlab-ce 7.2.0
- update to the sameersbn/ubuntu:14.04.20140818 baseimage
- remove /var/lib/apt/lists to optimize image size.
- disable UsePrivilegeSeparation in sshd configuration, fixes #122
- added OAUTH_BLOCK_AUTO_CREATED_USERS configuration option
- added OAUTH_ALLOW_SSO configuration option
- added github oauth configuration support
- added twitter oauth configuration support
- added google oauth configuration support
- added support for jira issue tracker
- added support for redmine issue tracker
- update to gitlab-shell 1.9.7
- update to the sameersbn/ubuntu:14.04.20140812 baseimage

**7.1.1**
- removed "add_header X-Frame-Options DENY" setting from the nginx config. fixes #110
- upgrade to gitlab-ce 7.1.1
- run /etc/init.d/gitlab as git user, plays nicely with selinux

**7.1.0**
- removed GITLAB_SUPPORT configuration option
- upgrade to gitlab-ce 7.1.0
- clone gitlab-ce and gitlab-shell sources from the git repo.
- disable pam authentication module in sshd
- update to the sameersbn/ubuntu:14.04.20140628 baseimage
- no more root access over ssh, use nsenter instead
- upgrade to nginx-1.6.x series from the nginx/stable ppa

**7.0.0**
- upgrade to gitlab-7.0.0
- fix repository and gitlab-satellites directory permissions.
- added GITLAB_RESTRICTED_VISIBILITY configuration option
- fix backup restore operation
- upgrade to gitlab-shell 1.9.6
- added app:sanitize command
- automatically migrate database when gitlab version is updated
- upgrade to gitlab-shell 1.9.5

**6.9.2**
- upgrade to gitlab-ce 6.9.2

**6.9.1**
- upgrade to gitlab-ce 6.9.1

**6.9.0**
- upgrade to gitlab-ce 6.9.0
- added GITLAB_RELATIVE_URL_ROOT configuration option
- added NGINX_MAX_UPLOAD_SIZE configuration to specify the maximum acceptable size of attachments.

**6.8.2**
- upgrade to gitlab-ce 6.8.2
- renamed configuration option GITLAB_SHELL_SSH_PORT to GITLAB_SSH_PORT
- added GITLAB_PROJECTS_VISIBILITY configuration option to specify the default project visibility level.
- generate and store ssh host keys at the data store.
- default GITLAB_PROJECTS_LIMIT is now set to 100
- use sameersbn/ubuntu:14.04.20140508 base image, the trusted build of sameersbn/ubuntu:14.04.20140505 seems to be broken
- use sameersbn/ubuntu:14.04.20140505 base image
- added CA_CERTIFICATES_PATH configuration option to specify trusted root certificates.
- added SSL support
- added SSL_DHPARAM_PATH configuration option to specify path of dhparam.pem file.
- added SSL_KEY_PATH configuration option to specify path of ssl key.
- added SSL_CERTIFICATE_PATH configuration option to specify path of ssl certificate
- added GITLAB_HTTPS_ONLY configuration option to configure strict https only access
- added SSL_SELF_SIGNED configuration option to specify use of self signed ssl certificates.
- fix git over ssh when the default http/https ports are not used.
- compile the assets only if it does not exist or if the gitlab version has changed.
- upgrade gitlab-shell to version 1.9.4
- cache compiled assets to boost application startup.
- fix symlink to uploads directory

**6.8.1**
- upgrade to gitlab-ce 6.8.1

**6.8.0**
- upgrade to gitlab-shell 1.9.3
- added GITLAB_SIGNIN setting to enable or disable standard login form
- upgraded to gitlab-ce version 6.8.0
- added support for linking with redis container.
- use sameersbn/ubuntu as the base docker image
- install postgresql-client to fix restoring backups when used with a postgresql database backend.

**6.7.5**
- upgrade gitlab to 6.7.5
- support linking to mysql and postgresql containers
- added DEFAULT_PROJECTS_LIMIT configuration option

**6.7.4**
- upgrade gitlab to 6.7.4
- added SMTP_AUTHENTICATION configuration option, defaults to :login.
- added LDAP configuration options.

**6.7.3**
- upgrade gitlab to 6.7.3
- install ruby2.0 from ppa

**6.7.2**
- upgrade gitlab to 6.7.2
- upgrade gitlab-shell to 1.9.1
- reorganize repo
- do not perform system upgrades (http://crosbymichael.com/dockerfile-best-practices-take-2.html)

**6.6.5**
- upgraded to gitlab-6.6.5

**v6.6.4**
- upgraded to gitlab-6.6.4
- added changelog
- removed postfix mail delivery
- added SMTP_DOMAIN configuration option
- added SMTP_STARTTLS configuration option
- added SMTP_DOMAIN configuration option
- added DB_PORT configuration option
- changed backup time to 4am (UTC)

**v6.6.2**
- upgraded to gitlab-6.6.2
- added automated daily/monthly backups feature
- documented ssh login details for maintenance tasks.
- perform upgrade of git, nginx and other system packages
- added GITLAB_SHELL_SSH_PORT configuration option
- added app:rake command for executing gitlab rake tasks
- documented hardware requirements

**v6.6.1**
- upgraded to gitlabhq-6.6.1
- reformatted README
