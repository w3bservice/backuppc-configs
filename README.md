# backuppc-configs
Sane default configurations for BackupPC

I find that every time I go to install a new instance of BackupPC or reinstall after a failure, I struggle to find sane default configuration for the exclude lists, so here is what I've come up with the most recent time.

The reference setup here is rsync to Linux clients with a share of '/', and rsyncd to Windows clients with a share of 'c'. Set the default for whichever type you use more. When you want to set up a client of the other type, simply change the backup method and share name, and the exclusions apply correctly without specifying them individually. When you have extra exclusions for a specific client, you can simply add them in the web interface and it works as expected.

The intent of this configuration is to back up all files that are possible to back up. While many of these files are not necessary to restore a system, it's also always possible that files end up in places you don't expect, and there is little overhead in backing them up. It's a "better safe than sorry" implementation that should work in most cases.

The reference Windows version is Windows 7, but this should work on most versions of Windows with little to no modification.
