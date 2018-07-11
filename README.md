# gate-cas-sso
Apereo CAS SSO Server with Gate MFA Sign-in and customized web pages for Sign-In

We use CAS Overlay gradle template

In addition to that 
- we add cas-gate plugin 
- add a custom login page

## Development Setup

If you have problem with permission denied while execute commands below, try to run it with `sudo`

- ./build.sh copy - to make sure config file is copied to default directory (/etc/cas/config)
- ./build.sh gencert - to generate dummy ssl certification so we can run it with https
- ./build.sh package - create cas.war (if you have problems with permissions denied try to run all commands with sudo)
- java -jar cas/build/libs/cas.war

## Configuration
By default configuration file will be on `/etc/cas/config/cas.properties`.
If you want to disable saml authentication feature, then you need to comment out `compile "org.apereo.cas:cas-server-support-saml-idp:${project.'cas.version'}"` inside `cas/build.gradle` and then try to rebuild it again.


