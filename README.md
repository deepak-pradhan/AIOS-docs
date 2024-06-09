# AIOS-docs

OS:
1. BIOS/UEFI Initialization:  
   , BIOS (Basic Input/Output System)  
   , UEFI (Unified Extensible Firmware Interface)  
  
   UEFI:  
   , initializes hardware components and. 
   , performs a Power-On Self Test (POST).  
   , looks for a bootable device
     (like a hard drive, SSD, or USB drive)  
   , loads the bootloader from that device. 
  
  Bootloader:
  GRUB, LILO, systemd-boot, ..
  ,loads OS kernel into memory
     ,may provide a BOOT menu
     , for selecting between OS
       or kernel configurations.
  , Kernersville Initialization 

  Kernel Initialization:
  , Linux kernel is loaded into memory
  , and starts executing
  , initializes hardware
     , mounts the root filesystem
       from bootloader configuration
  , starts the init process
    the first process is PID 1
   
  .init Process:
     old: from systemd, Upstart, or OpenRC in modern systems) is responsible for bringing up the user space and starting system services.init reads its configuration files (e.g., /etc/inittab for SysV init, or various unit files for systemd) and starts the necessary services and daemons.System Initialization Scripts:Depending on the init system, various scripts and services are started. For example:In SysV init, scripts in /etc/rc.d/ and /etc/init.d/ are executed.In systemd, unit files in /etc/systemd/system/ and /lib/systemd/system/ are processed.Login Process:After the system services and daemons are started, the system presents a login prompt (for graphical login managers like GDM, LightDM, or text-based getty processes).When a user logs in, the shell initialization files are processed.