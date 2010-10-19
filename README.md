ldapgetent
==========

Rationale
---------
ldapgetent implements a subset of the unix command [getent](http://en.wikipedia.org/wiki/Getent).
See usage below.

It can be used to synchronize local /etc/passwd and /etc/group files on systems that don't have
getent installed and that don't natively support PAM LDAP authentication. This is the
case on some NAS servers that don't come with a standard Linux distribution.

Usage
-----
Usage: ldapgetent database [key ...]
Currently database must be either 'passwd' or 'group'.

If the LDAP server can't be reached ldapgent will not produce any output on STDOUT. An error
message will be printed to STDERR.
