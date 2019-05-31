nagiosgraph
=========

An Ansible role that installs nagiosgraph.

Requirements
------------

Requires a working nagios installation.

See the nagiosgraph documentation for info on how to add nagiosgraph in your service templates etc.

Basically if you want a link to nagiosgraph to show for each service on the CGI GUI and also have a graph show 
up when you hover over the icon you need to add something like this in your generic template/s:

    action_url /nagiosgraph/cgi-bin/show.cgi?host=$HOSTNAME$&service=$SERVICEDESC$' onMouseOver='showGraphPopup(this)' onMouseOut='hideGraphPopup()' rel='/nagiosgraph/cgi-bin/showgraph.cgi?host=$HOSTNAME$&service=$SERVICEDESC$

That should really be all you need to do to your nagios config to get this role working.

Role Variables
--------------

See defaults/main.yml.

Dependencies
------------

No forced dependencies. Choose your preferred method of installing Nagios. You may wish to take a look at:

https://galaxy.ansible.com/oefenweb/nagios-server

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: monitoringservers
      roles:
         - { role: LukasGibb.nagiosgraph }

License
-------

MIT

Author Information
------------------

This role was created in 2019 by:
[Lukas Gibb](https://github.com/LukasGibb) from [CloudJourneyman.com](http://www.cloudjourneyman.com/)
