# Ways to list disks, partitions and filesystems in Linux
----------------------------------------------------------
There are several ways to list all the hard drives present in a system through Linux command lines.
Keep in mind a hard drive could be physically connected, virtually connected or even emulated.
There are other commands but these are probably the most commonly used and easy to get the job done.
Also note that some of these commands are actually disk partitioning tools and listing disk partition is one of their features.

Let’s see what commands you can use to show disk info in Linux.

#```1.df ``` 
df lists the actual “disk space usage” and it can give you information about what hard disks (or current disk space) is being used in the entire system.
The most common way to use it is with the -h argument which means “human readable”.Usage

```$df -h ```

#```2. fdisk```
fdisk lists the different partitions (which is related to hard drives as a hard drive can be divided into several partitions) in your system.Usage 
```$ sudo fdisk -l```

This will return the entire amount of space (in GB or MB), the entire amount of bytes and the entire amount of sectors per each partition and as a summary, it also gives you the start and end sectors, the amount of disk space (in Bytes) and the type of partition.

#```3. lsblk```

It is probably more visual than the others as it even shows the partitions per each disk in a visual way. It also gives information about the total size per each partition and disk and the physical location for each. This is very commonly used when you need to mount things to be used (like a USB stick or similar) so you can know where is it in order to proceed to mount it. Usage

```$lsblk```

#```4. cfdisk ```

cfdisk is probably the most advanced one in GUI (Graphical User Interface), as it is absolutely visual and interactive. It allows at first to list all disks/partitions in your system but it also allows you to manage them by selecting them and then applying actions such as “Delete”, “Resize”, “Type” (to change partition Type) and “Write” changes done to partitions.
It also gives you very friendly information about each partition and disk as it gives you where does each partition cylinders start and ends, amount of sectors used by each one and the full size of each one with its type. It won’t give you for example how much is used or free to use.Usage

```$ sudo cfdisk```

#```5. parted```

This one is similar to previous ones mentioned, it lists all partitions and allows to manage them. Its main difference is that it also informs you the brand and model of your hard disks and even the type of connectivity used in it (scsi, sata, etc) and total disk size. Usage

```$sudo parted -l```

#```6. sfdisk ```

This is very similar to fdisk, however sfdisk allows you to see both physical and logical volumes and also gives you a “summary” of the actual physical volumes’ partitions with the cylinders (start and end), sectors, size and type.The s stands for super user.Usage 

```$ sudo sfdisk -l```
