ec2util
=======

Performs common ec2 tasks on the command line. Written in Python, based on boto.

This is a naive implementation of the common tasks I have to perform regularly on ec2. 

It has a nice command line interface thanks to docopt.

Installation
------------

pip install ec2util


Usage
-----

Type ec2util after installation to get the command line help. Usage should be straightforward.

```
laszlocph@laszlocph:~/github/ec2util$ ec2util
Usage:
  ec2util print (instances|snapshots|amis|sgroups)
  ec2util print volumes [<instance_id>]
  ec2util (start|stop) <instance_id>
  ec2util attach <volume_id> <instance_id> <mapping>
  ec2util detach <volume_id>
  ec2util enlarge <volume_id> <size>
  ec2util create snapshot <volume_id> <name>
  ec2util create volume <size> <zone> [<snapshot_id>]
  ec2util config
  ec2util (-h | --help)
  ec2util --version

```

For example the following command starts an instance:
```
laszlocph@laszlocph:~/github/infi.docopt_completion$ ec2util stop i-aea3d0c5
Stopping instance i-aea3d0c5
...stopping
...stopping
...stopping
...stopping
...stopping
...stopping
...stopping
...stopping
...stopping
stopped
```

Extensibility
-------------

Thanks to docopt and boto extending the code with new commands should be fairly simple


License
-------
ec2util is licensed under the MIT License. See LICENSE file
