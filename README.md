# backup_incremental
Incremental Backup with TAR

# Usage
## create backups
To create a backup execute the following command. The tool decides on the basis of the existing files and the days until the next full backup whether a full backup or an incremental backup is to be created. By default it is 7 days.
 
-s [source path] => set path to the data

-t [target path] => set path to the backupstorage

-d => create backup (dump)

>./incr-backup -s /var/www/ -t /mnt/backup/ -d
 
-p [days] => set Days to next fullbackup

>./incr-backup -s /var/www/ -t /mnt/backup/ -d -p 7
 
## restore backup
To restore a backup execute the following command
 
>./incr-backup -t ~/tmp/www/ -s ~/tmp/mnt/backup/20220106/ -r
