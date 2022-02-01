# docker-volume-backup
Backup and restore script for docker volumes

## Usage

```
$ ./dvbk -<mode> -v <volume> -f <filename>
```

**mode:** (b)ackup / (r)estore
**volume:** volumes listed under `$ docker volume ls`
**filename:** name of file to be writen/read (extension will be .tar (no need to input it))

On restore mode, if volume exists, confirmation is needed to replace current volume.


### Example
#### backup mode
`$ ./dvbk -b -v prometheus_data -f prometheus`
#### restore mode
`$ ./dvbk -r -v prometheus_data -f prometheus`