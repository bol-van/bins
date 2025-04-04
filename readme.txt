Often used binaries for android and not only

for ncurses: terminfo = /etc/terminfo
linked to musl or glibc, not bionic. requires /etc/resolv.conf for network name resolution

openssh server:
1)
unpack openssh.tgz to /
chown -R root:root /data/var /data/root
ssh-keygen -A
2)
copy passwd, group and shadow to /etc
chmod 644 /etc/passwd /etc/group
chmod 600 /etc/shadow
3)
unpack shadow.tgz to /
passwd root
4)
/system/xbin/sshd

mc notice : subshell is not supported with android /system/bin/sh. use busybox sh instead.
