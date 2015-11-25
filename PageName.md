# Installing #

  1. Check out or download nr.functions
  1. Make it executable
```
chmod a+x nr.functions
```
  1. Create symlinks for commands.
```
ln -s nr.functions n2r
ln -s nr.functions r2n
```
  1. Test it.
```
[A00017456@login-00 noderange]$ ./r2n node[00-09]
node00 node01 node02 node03 node04 node05 node06 node07 node08 node09
[A00017456@login-00 noderange]$ ./r2n node[00-09],node12,node14
node00 node01 node02 node03 node04 node05 node06 node07 node08 node09 node12 node14
[A00017456@login-00 noderange]$ ./n2r node00 node01 node02 node03 node12 node14             
node[00-03],node12,node14
[A00017456@login-00 noderange]$ ./n2r node00 node01 node02 node03 node12 node14 node{10..31}
node[00-03],node[10-31]
```