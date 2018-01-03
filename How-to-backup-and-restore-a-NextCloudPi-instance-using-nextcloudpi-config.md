You may want to move your NCP instance to a larger drive or restore it after a hardware failure.

You can visit https://your-local-IP:4443 for NCP's web interface or start nextcloudpi-config from your NCP terminal by typing:

`sudo nextcloudpi-config`

![ ](https://user-images.githubusercontent.com/8775469/34511790-5bedb6f4-f05e-11e7-9d60-bba86e2c2166.png)

Move up and down with arrow-keys, use tab to select(execute) or finish(cancel)

We are going to use nc-backup to back-up our NC instance to a file.
![](https://user-images.githubusercontent.com/8775469/34511800-664637ac-f05e-11e7-995c-f23e05d143ed.png)

The output will confirm if operation was successful and where the backup file is stored.

You may run backups automatically using nc-backup-auto
![](https://user-images.githubusercontent.com/8775469/34511804-692730ac-f05e-11e7-9ab0-f0ad3500d4df.png)
To enable/disable, type yes/no in the 'active' field, and adjust other settings to your needs 

We now have backups of our NC installation directory and database, no actual data included yet. Next is a backup of the configuration files.
![](https://user-images.githubusercontent.com/8775469/34511805-6b475358-f05e-11e7-84a8-bb9b48995efd.png) 
Select destination for backup of configuration:
![](https://user-images.githubusercontent.com/8775469/34511811-72e6c85a-f05e-11e7-803f-bf306a539cf6.png)
![](https://user-images.githubusercontent.com/8775469/34511813-74e6f3aa-f05e-11e7-9b41-40f9535606a9.png)

We now have backups of our NC installation directory, database and the configuration files. 
Still no actual data included yet. Next is a backup or rather BTRFS snapshot of our ncdata-directory.
Note: This will only work if you used BTRFS instead of ext4 when formating your NC data partition.
![](https://user-images.githubusercontent.com/8775469/34511814-776e2dfa-f05e-11e7-8b42-fc4ed7a777df.png) 
![](https://user-images.githubusercontent.com/8775469/34511817-7a0bae8e-f05e-11e7-86fa-9866889b36c4.png)
![](https://user-images.githubusercontent.com/8775469/34511818-7c1d397c-f05e-11e7-86bc-88d5e3f4fc3c.png)
It will confirm the name and location of the snapshot taken upon completion.
You may want to enable nc-snapshot-auto to have regular snapshots taken automatically.

..............
This a a work in progress, thank you for your patience ;-)