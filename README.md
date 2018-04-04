# astropy-hdfs
Modified Astropy code, able to open FITS files stored in a Hadoop Cluster (HDFS).

In order to stablish communication with HDFS, I used hdfs3.
The opening is made with the same function, .open(), the difference being that to
open files in HDFS the function should be called with the HDFS file path and the hadoop kwarg needs to be specified as True.

Example: .open('HDFS_file_path', hadoop=True)

To open the file, one copy is made in the local file system. After copying it, the local file is opened normally.
