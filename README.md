# docker
docker
$ docker run hello-world

$ docker pull continuumio/miniconda3
Using default tag: latest
latest: Pulling from continuumio/miniconda3
c73ab1c6897b: Pull complete
f4ee34443c42: Pull complete
58b0086c24cb: Pull complete
ca12d7eb7bff: Pull complete
de88fa640631: Pull complete
Digest: sha256:b3e76ca0bda1714f2e8447d807e5880a28ac07b18433cd19ed47c3da623993ae
Status: Downloaded newer image for continuumio/miniconda3:latest

Hyunjong@HYUNJONG_SEO MINGW64 /c/Program Files/Docker Toolbox
$ docker run -i -t continuumio/miniconda3 /bin/bash
(base) root@a28608122e77:/# ls -al
total 72
drwxr-xr-x  38 root root 4096 Mar 25 13:36 .
drwxr-xr-x  38 root root 4096 Mar 25 13:36 ..
-rwxr-xr-x   1 root root    0 Mar 25 13:36 .dockerenv
drwxr-xr-x   2 root root 4096 Mar 24 11:25 bin
drwxr-xr-x   2 root root 4096 Feb 23 23:23 boot
drwxr-xr-x   5 root root  360 Mar 25 13:36 dev
drwxr-xr-x  47 root root 4096 Mar 25 13:36 etc
drwxr-xr-x   2 root root 4096 Feb 23 23:23 home
drwxr-xr-x  10 root root 4096 Mar 24 11:25 lib
drwxr-xr-x   2 root root 4096 Mar 12 00:00 lib64
drwxr-xr-x   2 root root 4096 Mar 12 00:00 media
drwxr-xr-x   2 root root 4096 Mar 12 00:00 mnt
drwxr-xr-x   3 root root 4096 Mar 24 11:25 opt
dr-xr-xr-x 155 root root    0 Mar 25 13:36 proc
drwx------   3 root root 4096 Mar 24 11:26 root
drwxr-xr-x   4 root root 4096 Mar 12 00:00 run
drwxr-xr-x   2 root root 4096 Mar 12 00:00 sbin
drwxr-xr-x   2 root root 4096 Mar 12 00:00 srv
dr-xr-xr-x  13 root root    0 Mar 25 13:36 sys
drwxrwxrwt   2 root root 4096 Mar 24 11:25 tmp
drwxr-xr-x  17 root root 4096 Mar 24 11:26 usr
drwxr-xr-x  14 root root 4096 Mar 24 11:25 var
(base) root@a28608122e77:/# python3 -c "print(3*5)"
15
(base) root@a28608122e77:/# pip install beautifulsoup4
Collecting beautifulsoup4
  Downloading beautifulsoup4-4.6.0-py3-none-any.whl (86kB)
    100% || 92kB 801kB/s
Installing collected packages: beautifulsoup4
Successfully installed beautifulsoup4-4.6.0
You are using pip version 9.0.1, however version 9.0.3 is available.
You should consider upgrading via the 'pip install --upgrade pip' command.
(base) root@a28608122e77:/# pip install requests

$ docker ps -a
CONTAINER ID        IMAGE                    COMMAND                  CREATED
          STATUS                      PORTS               NAMES
a28608122e77        continuumio/miniconda3   "/usr/bin/tini -- /b"   7 minutes a
go       Exited (0) 15 seconds ago                       lucid_haibt
9e2e8ec9b1b8        hello-world              "/hello"                 23 minutes
 ago      Exited (0) 23 minutes ago                       cranky_hodgkin

Hyunjong@HYUNJONG_SEO MINGW64 /c/Program Files/Docker Toolbox
$ docker commit a28608122e77 mlearn:init
sha256:71520882d87ab874f2c4d62e5eb01faab660c9e1bba047389f68878e6abbca13

Hyunjong@HYUNJONG_SEO MINGW64 /c/Program Files/Docker Toolbox
$ docker run -i -t mlearn:init
(base) root@97b14aa6042f:/#

Hyunjong@HYUNJONG_SEO MINGW64 /c/Program Files/Docker Toolbox
$ docker run -i -t -v /c/Users/Hyunjong/sample:/sample mlearn:init
(base) root@31d5514aecf0:/# ls -al
total 72
drwxr-xr-x  43 root root  4096 Mar 25 14:35 .
drwxr-xr-x  43 root root  4096 Mar 25 14:35 ..
-rwxr-xr-x   1 root root     0 Mar 25 14:35 .dockerenv
drwxr-xr-x   2 root root  4096 Mar 24 11:25 bin
drwxr-xr-x   2 root root  4096 Feb 23 23:23 boot
drwxr-xr-x   5 root root   360 Mar 25 14:35 dev
drwxr-xr-x  47 root root  4096 Mar 25 14:35 etc
drwxr-xr-x   2 root root  4096 Feb 23 23:23 home
drwxr-xr-x  10 root root  4096 Mar 24 11:25 lib
drwxr-xr-x   2 root root  4096 Mar 12 00:00 lib64
drwxr-xr-x   2 root root  4096 Mar 12 00:00 media
drwxr-xr-x   2 root root  4096 Mar 12 00:00 mnt
drwxr-xr-x   4 root root  4096 Mar 25 13:42 opt
dr-xr-xr-x 155 root root     0 Mar 25 14:35 proc
drwx------   4 root root  4096 Mar 25 14:35 root
drwxr-xr-x   4 root root  4096 Mar 12 00:00 run
drwxrwxrwx   1 1000 staff    0 Mar 25 14:33 sample
drwxr-xr-x   2 root root  4096 Mar 12 00:00 sbin
drwxr-xr-x   2 root root  4096 Mar 12 00:00 srv
dr-xr-xr-x  13 root root     0 Mar 25 13:37 sys
drwxrwxrwt   2 root root  4096 Mar 25 13:43 tmp
drwxr-xr-x  17 root root  4096 Mar 24 11:26 usr
drwxr-xr-x  14 root root  4096 Mar 24 11:25 var
(base) root@31d5514aecf0:/# cd sample
(base) root@31d5514aecf0:/sample# ls -a
.  ..  test.txt
(base) root@31d5514aecf0:/sample# cat test.txt
docker mount
docker run -i -t -v /c/Users/Hyunjong/sample:/sample mlearn:inti
(base) root@31d5514aecf0:/sample# exit
exit

Hyunjong@HYUNJONG_SEO MINGW64 /c/Program Files/Docker Toolbox
$ docker run -i -t -v /c/Users/Hyunjong/sample:/sample mlearn:init
(base) root@2aa704d3a538:/#
(base) root@b18c51d6220d:/sample# python download-png.py
(base) root@b18c51d6220d:/sample# ls -l
total 57
-rwxrwxrwx 1 1000 staff   138 Mar 26 13:12 download-
-rwxrwxrwx 1 1000 staff 56621 Mar 26 13:18 test.png
-rwxrwxrwx 1 1000 staff    80 Mar 25 14:34 test.txt
