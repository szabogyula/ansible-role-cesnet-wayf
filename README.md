szabogyula.cesnet-wayf
========

Install and configure CESNET WAYF service

Requirements
------------

Role Variables
--------------

source_git_url: https://github.com/CESNET/wayf.git

document_root:  /var/www/html

wayf_theme: false

DEVEL: false

basedir: /opt/getMD

configdir: "{{ basedir }}/etc"

feedList: "{{ configdir}}/feeds"

signerDir: "{{ configdir }}/signers"

lockFile: /var/run/getMD.lock

vardir: "{{ basedir }}/var"

pubBase: "{{ vardir }}/pub"

downloadBase: "{{ vardir }}/download"

cacheDir: "{{ vardir }}/cache"

oldPubBase: "{{ vardir }}/old"

logoPubBaseURI: logoPubBaseURITODO

libdir: "{{ basedir }}/lib"

xslFile:  "{{ libdir }}/md2json.xsl"

logoPredefDir: "{{ libdir }}/logo"

sqlite_schema: "{{ libdir }}/SPDBDef2.sql"

sqlite_db: "{{ pubBase }}/current/lib/SPReg.sqlite"

wget: /usr/bin/wget

sqlite: /usr/bin/sqlite3

xsltproc: /usr/bin/xsltproc

xmlsec: /usr/bin/xmlsec1

max_width: 1000

max_height: 1000

max_age: 86000

min_kept: 6

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
-------------------------

    - hosts: servers
      roles:
         - { role: szabogyula.cesnet-wayf }

License
-------

GNU GPLv3

Author Information
------------------

Gyula Szabó
gyula.szabo@sztaki.mta.hu
