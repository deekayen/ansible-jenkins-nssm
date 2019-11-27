Jenkins Windows NSSM Service
===============

Manage the Jenkins service on Windows with NSSM.

Requirements
------------

A vault password. The vault password in this sample repository is `hunter2`.

Role Variables
--------------

```
chocolatey_packages:
  - 7zip
  - curl
  - dotnet4.5
  - git
  - groovy
  - notepadplusplus
  - nsis
  - nssm
  - powershell
  - python2
  - python3
  - svn
  - vmware-tools
  - webdeploy
  - windbg
  - winmerge
  - winscp
  - wixtoolset

jenkins_path: C:\Jenkins\jenkins.exe
jenkins_user: ""
jenkins_password: ""
```

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: jenkins

      pre_tasks:
        - action: win_ping

      roles:
        - packages
        - jenkins

License
-------

BSD
