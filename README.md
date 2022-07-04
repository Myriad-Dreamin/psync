
## PSync

## Usage

```shell
 $ ./psync --help
usage: psync [-h] [-v] [--dry] [--digest_fn {file_name,md5,ctime,atime,mtime}] -c CONFIG

python sync

optional arguments:
  -h, --help            show this help message and exit
  -v, --verbose         show verbose status
  --dry                 dry run
  --digest_fn {file_name,md5,ctime,atime,mtime}
                        the digest method using for checking files
  -c CONFIG, --config CONFIG
                        get sync arguments
```

## Config Example

```ini
[vars]
audio = deployment/www/statics/audio
www = deployment/www

[configs]
remote_host = pixel-master
remote_root = /home/pixel
local_root = /mnt/hdd-9737f991/Storage/Backup/Pixel
directories =
  ${configs:remote_root}/${vars:audio}/2018
  ${configs:remote_root}/${vars:audio}/2019
  ${configs:remote_root}/${vars:audio}/2020
  ${configs:remote_root}/${vars:audio}/2021
  ${configs:remote_root}/${vars:audio}/2022
  ${configs:remote_root}/${vars:www}/
```

