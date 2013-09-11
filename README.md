apache-hadoop-scripts
=====================

Some personal tweaks to the Apache Hadoop scripts bundled into the debian package.

When installing official debian packages from Apache, there are certain things missing ;
from my memory, the users hdfs and mapred, and the group hadoop are not created.
I am as well unsure that the /var/lib/hadoop and the /var/log/hadoop directories are
correctly created (with the correct permissions) either.

In addition, there seems to be a mismatch between the variable HADOOP_IDENT_STRING, which
seems to permit giving a name to the cluster. The apache scripts try to change ownership of
some files with the variable content.

This repository is meant to keep somewhere the different modifications I had to provide before
being able to launch an hadoop cluster (3 datanodes, 1 namenode, 1 jobtracker and 3
tasktrackers).
