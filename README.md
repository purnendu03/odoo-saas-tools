[![Build Status](http://runbot.it-projects.info/runbot/badge/flat/odoo-saas-tools/10.0.svg)](http://runbot.it-projects.info/demo/odoo-saas-tools/10.0)

odoo-saas-tools
===============

System to sale and manage odoo databases.

Requirements
============

To start SaaS system you need:

* ubuntu/debian OS
* [installed odoo](http://odoo-development.readthedocs.io/en/latest/admin/install.html)
* [configured nginx](docs/port_80.rst) 
* [installed dependencies](docs/dependencies.rst)
* [correctly configured odoo](docs/odoo-configuration.rst) 
* records in /etc/hosts, if you install it locally, or dns records otherwise:

    > sudo bash -c "python saas.py --print-local-hosts >> /etc/hosts"

Build and run
=============

Execute saas.py script and wait some time

> python saas.py --portal-create --server-create --plan-create --run --odoo-script=/path/to/openerp-server --odoo-config=/path/to/openerp-server.config

>
python saas.py --portal-create --portal-db-name=missborilnih.si --server-create --server-db-name=server.missborilnih.si --run --odoo-script=/odoo10/odoo10-server/odoo-bin --odoo-config=/etc/odoo10-server.conf --odoo-data-dir=/odoo10/.local/share/Odoo/filestore/


SaaS local:
keep adding the new instance url to /etc/hosts

python /home/psi/modules/chau_le/odoo-saas-tools/saas.py --portal-create --portal-db-name=saas-portal-10.local --server-create --server-db-
name=server-1.saas-portal-10.local --run --odoo-script=/home/psi/sources/odoo_10/odoo-bin --odoo-config=/etc/odoo10-serverr.conf --odoo-data-dir=/opt/odoo10/.local/share/Odoo/filestore/

python /home/hiren/workhome/odoo-10/odoo-bin --config=/etc/odoo-saas.conf --xmlrpc-port=8069 --longpolling-port=8072 --db-filter=%h

Warn: Can't find .pfb for face 'Times-Roman'


The SaaS system is ready! Try, for example, open start page:

* http://saas-portal-9.local/page/start?plan_id=1

Links
=====

* Features: [docs/features.rst](docs/features.rst)
* API integration: [docs/api.rst](docs/api.rst)
* Development: [docs/development.rst](docs/development.rst)
