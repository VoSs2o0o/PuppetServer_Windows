Compose File for Puppet Community, which is running on Docker for Windows.

# Installation
Simply clone it to a Directory, and do a: 

    docker compose up
    
Your code Dir (/etc/puppetlabs/code) is mapped to <MyDir>\data\puppet-code\

# Contents

A complete Puppetstack, which is running in Docker on Windows.
Puppetexplorer is also included. 

You can set some configs in the .env-file:

    PUPPETSERVER_HOSTNAME (puppet)
    DNS_ALT_NAMES (puppet)
    ADDITIONAL_COMPOSE_SERVICES_PATH (./data)
    POSTGRES_IMAGE (postgres:12.6)
    PUPPETDB_IMAGE (puppet/puppetdb:latest)
    PUPPETSERVER_IMAGE (puppet/puppetserver:latest)
    PUPPETBOARD_IMAGE (bootc/puppetboard:latest)
    PUPPERWARE_ANALYTICS_ENABLED (true)
    RESTART_BEHAVIOR (always) possible are: "no", always, on-failure, unless-stopped
[see docs for restart](https://github.com/compose-spec/compose-spec/blob/master/spec.md#restart)

variables from the images:
there are more varibales you can set, see on:

[hub.docker puppetserver](https://hub.docker.com/r/puppet/puppetserver/)

CA_HOSTNAME is important here...

[hub.docker puppetdb](https://hub.docker.com/r/puppet/puppetdb/)

[hub.docker postgres](https://hub.docker.com/_/postgres)


compose variables:

    COMPOSE_PROJECT_NAME (puppetmaster)

# original code used

I have simply used the code from [Puppet Pupperware](https://github.com/puppetlabs/pupperware), 
extract the Code for the Community Edition, integrated all the manual stuff to .env-file, and
have added newer version of puppetboard (not the puppet/puppetboard one)

# License
[Apache 2.0](LICENSE.txt) 
