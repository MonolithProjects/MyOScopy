### How to use myoscopy...

```
myoscopy [OPTIONS]... [-d|--to-disk=<partition>]
```

##### Options:
```
-d <partition>, --to-disk=<partition> Start OSCopy to destionation.
                                      If you are using LVM partition as the destination, use path /dev/mapper/...
-S, --shutdown        Shutdown after backup
-x, --no-email        Report will be not sent via email
-c, --clear           Can be used after interrupted backup
-n, --no-delete       Do NOT delete previous backup data. Will update current backup
                      Keep in mind that rsync nees some free space for temporarry files
-s, --show            Show last backup info
-f, --forcee          Force backup and suppress all warnings
-v, --version         Show MyOScopy version
    --debug           Debug mode
-h, --help            This Help page
```

##### Example:
```
myoscopy --to-disk=/dev/sdb1
myoscopy -Sxd /dev/sdb1
myoscopy -S -f -d /dev/mapper/backup_vg-backup_lv
```
