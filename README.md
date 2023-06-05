# OSlab
labwork for Operating system course
# WEEEK2 
```
cd ~
sudo apt-get update
    4  sudo apt-get upgrade
    5  cd ~
    6  sudo apt update && sudo apt upgrade -y
    7  touch test.txt
    8  nano test.txt
    9  cd OSlab
   10  cd Dekstop/OSlab
   11  cd Desktop
   12  ls
   13  cd OSlab
   14  cd ~
   15  cd /Desktop/OSlab
   16  cd /Desktop/OSlab/
   17  cd Desktop/OSlab/
   18  nano test.txt
   19  nano week2.sh
   20  ls
   21  git add test.txt
   22  git commit -m "Add test file"
   23  git push origin main
   24  git remote -v
   25  git push origin main
   26  git pull
   27  git pull main
   28  git pull https://github.com/ULUGBEK12194914/OSlab.git main
   29  git push https://ULUGBEK12194914:<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>@github.com/ULUGBEK12194914/OSlab.git
   30  git push https://ULUGBEK12194914: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@github.com/ULUGBEK12194914/OSlab.git
   31  git pull origin main
   32  git remote add origin https://github.com/ULUGBEK12194914/OSlab.git
   33  git remote -v
   34  git pull origin main
   35  git add .
   36  git comming -m "Your comming"
   37  git commit -m "Your comming"
   38  ls
   39  git add test.txt
   40  git commit -m "Test file added"
   41  git init
   42  echo "Hello, world" > hello.txt
   43  ls
   44  git add hello.txt
   45  git commit -m "Add hello.txt file"
   46  git remote add origin https://github.com/ULUGBEK12194914/OSlab.git
   47  git push -u origin main
   48  git remote set-url origin https://github.com/ULUGBEK12194914/OSlab.git
   49  git push -u origin main
   50  git fetch
   51  git status
   52  git merge origin/main
   53  git merge origin/main --allow-unrelated-histories
   54  git push -u origin main
   55  ls
   56  rm week2.sh
   57  ls
   58  history > week2.sh
   ```
   # WEEK3
   ### FILE MANAGEMENT
   ```
  172  cd
  173  mkdir Videos/Watched
  174  ls
  175  ls -R Videos
  176  cd Documents
  177  mkdir ProjectX ProjectY
  178  ls
  179  mkdir -p Thesis/Chapter1 Thesis/Chapter2 Thesis/Chapter3
  180  cd
  181  ls -R Videos Documents
  182  cd Videos
  183  cp blockbuster1.ogg blockbuster3.ogg
  184  cd ../Documents
  185  cp thesis_chapter1.odf thesis_chapter2.odf Thesis ProjectX
  ```
![]()

# WEEK 6
### Redirecting Output to a File or Program
```
parallels@ubuntu-linux-22-04-desktop:~/Documents$ cd ..
parallels@ubuntu-linux-22-04-desktop:~$ date > /tmp/saved-timestamp
parallels@ubuntu-linux-22-04-desktop:~$ tail -n 100 /var/log/dmesg > /tmp/last-100-boot-messages
parallels@ubuntu-linux-22-04-desktop:~$ cat file1 file2 file3 file4 > /tmp/all-four-in-one
cat: file1: No such file or directory
cat: file2: No such file or directory
cat: file3: No such file or directory
cat: file4: No such file or directory
parallels@ubuntu-linux-22-04-desktop:~$ mkdir file1 file2 file3 file4
parallels@ubuntu-linux-22-04-desktop:~$ cat file1 file2 file3 file4 > /tmp/all-four-in-one
cat: file1: Is a directory
cat: file2: Is a directory
cat: file3: Is a directory
cat: file4: Is a directory
parallels@ubuntu-linux-22-04-desktop:~$ rm -rf file1 file2 file3
parallels@ubuntu-linux-22-04-desktop:~$ ls
Desktop    Downloads  Music  Pictures  snap       test.txt  vip   week3.sh
Documents  file4      nurse  Public    Templates  Videos    vip1
parallels@ubuntu-linux-22-04-desktop:~$ cat > file1 file2 file3 file4 > /tmp/all-four-in-one
cat: file2: No such file or directory
cat: file3: No such file or directory
cat: file4: Is a directory
parallels@ubuntu-linux-22-04-desktop:~$ rm -rf file1 file2 file3 file4
parallels@ubuntu-linux-22-04-desktop:~$ cat > file1 file2 file3 file4
cat: file2: No such file or directory
cat: file3: No such file or directory
cat: file4: No such file or directory
parallels@ubuntu-linux-22-04-desktop:~$ cat > file2
^C  
parallels@ubuntu-linux-22-04-desktop:~$ cat > file3
^C
parallels@ubuntu-linux-22-04-desktop:~$ cat > file4
^C
parallels@ubuntu-linux-22-04-desktop:~$ cat > file1 file2 file3 file4 > /tmp/all-four-in-one
parallels@ubuntu-linux-22-04-desktop:~$ ls -a > /tmp/my-file_names
parallels@ubuntu-linux-22-04-desktop:~$ echo "new line of information" >> /tmp/many-lines-of-information
parallels@ubuntu-linux-22-04-desktop:~$ diff previous-file current-file >> /tmp/tracking-changes-made
diff: previous-file: No such file or directory
diff: current-file: No such file or directory
parallels@ubuntu-linux-22-04-desktop:~$ cat > previous-file
^C
parallels@ubuntu-linux-22-04-desktop:~$ cat > current-file
^[[A^C
parallels@ubuntu-linux-22-04-desktop:~$ diff previous-file current-file >> /tmp/tracking-changes-made
parallels@ubuntu-linux-22-04-desktop:~$ find /etc -name passwd 2> /tmp/errors
/etc/passwd
/etc/pam.d/passwd
parallels@ubuntu-linux-22-04-desktop:~$ find /etc -name passwd > /tmp/output 2> /tmp/errors
parallels@ubuntu-linux-22-04-desktop:~$ find /etc -name passwd > /tmp/output 2> /dev/null
parallels@ubuntu-linux-22-04-desktop:~$ find /etc -name passwd &> /tmp/save-both
parallels@ubuntu-linux-22-04-desktop:~$ find /etc -name passwd >> /tmp/save-both 2>&1
parallels@ubuntu-linux-22-04-desktop:~$ la -l /usr/bin | less

[1]+  Stopped                 ls --color=auto -A -l /usr/bin | less
parallels@ubuntu-linux-22-04-desktop:~$ ls | wc -l
20
parallels@ubuntu-linux-22-04-desktop:~$ ls -t | head -n 10 > /tmp/ten-last-changed-files
parallels@ubuntu-linux-22-04-desktop:~$ ls > /tmp/saved-output | less

[2]+  Stopped                 ls --color=auto > /tmp/saved-output | less
parallels@ubuntu-linux-22-04-desktop:~$ ls -l | tee /tmp/saved-output | less
```
![]()
```

[3]+  Stopped                 ls --color=auto -l | tee /tmp/saved-output | less
parallels@ubuntu-linux-22-04-desktop:~$ id
uid=1000(parallels) gid=1000(parallels) groups=1000(parallels),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),110(lxd)
parallels@ubuntu-linux-22-04-desktop:~$ ls -l /tmp
total 252
-rw-rw-r-- 1 parallels parallels     0 Jun  6 00:00 all-four-in-one
-rw-rw-r-- 1 parallels parallels   240 Jun  6 00:04 errors
drwxr-xr-x 2 root      root       4096 Jun  5 16:53 hsperfdata_root
-rw-rw-r-- 1 parallels parallels 11184 Jun  5 23:56 last-100-boot-messages
-rw-rw-r-- 1 parallels parallels    24 Jun  6 00:01 many-lines-of-information
-rw-rw-r-- 1 parallels parallels   300 Jun  6 00:01 my-file_names
-rw-rw-r-- 1 parallels parallels    30 Jun  6 00:04 output
-rw------- 1 root      root          0 Jun  5 17:25 prl_nettool.lock
-rw-rw-r-- 1 parallels parallels   540 Jun  6 00:05 save-both
-rw-rw-r-- 1 parallels parallels  1185 Jun  6 00:08 saved-output
-rw-rw-r-- 1 parallels parallels    32 Jun  5 23:56 saved-timestamp
drwx------ 3 root      root       4096 Jun  5 03:10 snap-private-tmp
drwx------ 3 root      root       4096 Jun  5 03:09 systemd-private-cf8fc642f4534c3c8cb9ae821a398795-colord.service-P8pkbo
drwx------ 3 root      root       4096 Jun  5 03:09 systemd-private-cf8fc642f4534c3c8cb9ae821a398795-geoclue.service-PRN9rg
drwx------ 3 root      root       4096 Jun  5 03:09 systemd-private-cf8fc642f4534c3c8cb9ae821a398795-ModemManager.service-Zlp5bD
drwx------ 3 root      root       4096 Jun  5 03:09 systemd-private-cf8fc642f4534c3c8cb9ae821a398795-power-profiles-daemon.service-CY5BI2
drwx------ 3 root      root       4096 Jun  5 03:09 systemd-private-cf8fc642f4534c3c8cb9ae821a398795-switcheroo-control.service-YyO8bv
drwx------ 3 root      root       4096 Jun  5 03:09 systemd-private-cf8fc642f4534c3c8cb9ae821a398795-systemd-logind.service-BIHFjr
drwx------ 3 root      root       4096 Jun  5 16:52 systemd-private-cf8fc642f4534c3c8cb9ae821a398795-systemd-oomd.service-YylSEk
drwx------ 3 root      root       4096 Jun  5 16:52 systemd-private-cf8fc642f4534c3c8cb9ae821a398795-systemd-resolved.service-xH8fm7
drwx------ 3 root      root       4096 Jun  5 16:52 systemd-private-cf8fc642f4534c3c8cb9ae821a398795-systemd-timesyncd.service-72jc2m
drwx------ 3 root      root       4096 Jun  5 03:09 systemd-private-cf8fc642f4534c3c8cb9ae821a398795-upower.service-4lUmvB
-rw------- 1 parallels parallels    32 Jun  5 17:18 temp0RIG7X
-rw------- 1 parallels parallels    32 Jun  5 17:19 temp1WMKof
-rw------- 1 parallels parallels    32 Jun  5 17:19 temp49WQG3
-rw------- 1 parallels parallels    32 Jun  5 18:46 temp9KlGsl
-rw------- 1 parallels parallels    32 Jun  5 22:56 temp9TYh2Z

-rw------- 1 parallels parallels    32 Jun  5 23:36 tempXXKPlO
-rw------- 1 parallels parallels    32 Jun  5 23:09 tempYpnaNw
-rw------- 1 parallels parallels    32 Jun  5 23:36 tempzEB2b2
-rw-rw-r-- 1 parallels parallels    86 Jun  6 00:07 ten-last-changed-files
drwx------ 2 root      root       4096 Jun  5 16:52 tmp.ZzimFfTE9x
drwx------ 2 parallels parallels  4096 Jun  5 23:52 tracker-extract-3-files.1000
drwx------ 2 gdm       gdm        4096 Jun  5 03:09 tracker-extract-3-files.129
-rw-rw-r-- 1 parallels parallels     0 Jun  6 00:02 tracking-changes-made
drwxr-xr-x 2 root      root       4096 Jun  5 16:54 ubuntu-advantage
parallels@ubuntu-linux-22-04-desktop:~$ 
```
# WEEK 7
