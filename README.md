[![Build Status](https://travis-ci.org/wrouesnel/docker.guacomole.svg?branch=master)](https://travis-ci.org/wrouesnel/docker.guacomole)

# Apache Guacomole for Standalone Deployment

## LDAP Parameters

## WebUI Hooks

The following webui hooks are available to carry out container operations,
protected behind the admin interface and require POST commands:

## Environment Variables

* `HOSTNAME`
  Persistent hostname of this node. If unset defaults to the docker hostname.

* `ADMIN_USER=admin`
  Username of the admin user for accessing online management functions of the
  container (namely, the WebUI of alertmanager and cockroachdb).

* `ADMIN_PASSWORD`
  Password of the admin user for accessing online management functions of the
  container (namely, the WebUI of alertmanager and cockroachdb).

* `WEBUI_DNS_NAME`
  DNS name which the Web UI is being hosted under.

* `WEBUI_SSL_SERVER_CERT=`
  WebUI server identity certificate. May be a literal PEM certificate or a file path
  inside the container.
* `WEBUI_SSL_SERVER_KEY=`
  WebUI server identity key. May be a literal PEM certificate or a file path
  inside the container.
* `WEBUI_SSL_SERVER_CERTCHAIN=`
  WebUI server identity certificate chain. May be a literal PEM certificate or a file path
  inside the container.

* `SMTP_SMARTHOST=`
  `hostname:port` to use for sending alert emails.
* `SMTP_FROM`
  from address to set for from emails. If unset, defaults to `alerts@{{API_DNS_NAME}}`
* `SMTP_USERNAME=`
  username to use to login to the SMTP server.
* `SMTP_PASSWORD=`
  password to use to login to the SMTP server.
  
* `ALERT_EMAIL_ADDRESS=`
  email address to send alerts to.


## Hacking

`make run-it` to startup the container with most dev options enabled.
`make enter-it` to override the entrypoint and get a shell.
`make exec-into` will try and start a shell in an already running container.
