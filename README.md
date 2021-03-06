# MYSTATS

## 1.0 Introduction
This repository contains two versions of the MyStats utility. This reports on the resource usage between two snapshots in an active database session. It is a combination of Jonathan Lewis's SNAP_MY_STATS package and my own re-factoring of Tom Kyte's runstats utility (also available via www.oracle-developer.net or github.com/oracle-developer/runstats). I've also added some functionality and flexibility around the statistics reporting section.

## 2.0 Versions
There are two versions provided.

### 2.1 mystats_pkg.sql
This creates via a single PL/SQL package named MYSTATS_PKG. This uses invoker rights and dynamic SQL to workaround the common issue whereby developers are not given explicit grants on the required V$ views but have V$ access via a role. See the comments in the package header for more details and usage instructions.

### 2.2 mystats.sql
This version is a standalone SQL*Plus script that runs MyStats from your SQLPATH without the need to create any database objects. This can be used if you are not able to create the PL/SQL package version of MyStats. See the comments in the script header for more details and usage instructions.

## 3.0 Version History
```
Version  Date            Description
-------- --------------- ----------------------------------------------
1.0      June 2007       Original version
1.1      January 2009    Added extended reporting options
2.0      October 2011    Re-design for standalone script version
2.01     November 2011   Bug-fix for numeric overflow
3.0      November 2015   Added extended snapshot and reporting options
```

## 4.0 Credits
1. Credit is given to Jonathan Lewis for his original idea of taking two snapshots to identify resource consumption.
2. Thanks to Martin Bach for suggesting (and providing a prototype) for extended snapshot and reporting options.

## 5.0 License
This project uses the MIT License.
See https://github.com/oracle-developer/mystats/blob/master/LICENSE

Adrian Billington
(c) www.oracle-developer.net