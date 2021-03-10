PBIS
=========

Ansible role for deploying PowerBroker Identity Services (PBIS).


Role Variables
--------------

**defaults/main.yml**

- **pbis_enterprise_version** : Use enterprise or open version (boolean)
- **pbis_config** : Configure PBIS (boolean)
- **pbis_config_AssumeDefaultDomain** : PBIS config AssumeDefaultDomain (boolean)
- **pbis_config_HomeDirTemplate** : PBIS config HomeDirTemplate (string)
- **pbis_config_RequireMembershipOf** : PBIS config RequireMembershipOf  (list)
- **pbis_config_LoginShellTemplate** : PBIS config LoginShellTemplate (string)
- **pbis_config_DisplayMotd** : PBIS config DisplayMotd (boolean in string)
- **pbis_config_UserIgnore** : List of users for local and not LDAP connection (list)
- **pbis_join** : Join domain with PBIS (boolean)
- **pbis_domain** : Domain to join (string)*
- **pbis_join_user** : User for domain join (string)*
- **pbis_join_password** : Password for domain join (string)*
- **pbis_join_ou** : OU to join, not used when not defined

**vars/\***

Vars in vars/* files start with `pbis_` and are required to determine repo url and package name. 

**External**

- **showpass** : Show log on pbis join when defined

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: thystips.pbis, tags: pbis }

License
-------

GPLv3

Author Information
------------------

Antoine Thys
contact@antoinethys.com
