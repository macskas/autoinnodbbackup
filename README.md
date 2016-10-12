# autoinnodbbackup
automysqlbackup innobackupex alternative. for easy bacula backup

## usage
set the backup directory, mysql user, mysql password in the configuration file

```
/usr/local/bin/autoinnodbbackup [option]
        -h: show help
        -q: silent mode
        -u: update from github (master)
        -c <config>: read a config file
```

### bacula
example fileset configuration:
```
FileSet {
  Name = "AutoMysqlBackupFiles"
  Include {
    Options {
      signature = MD5
    }
    File = /backup/latest
  }
}
```
