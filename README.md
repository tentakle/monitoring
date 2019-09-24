# monitoring
By default, the Cgroup memory controller is in the state missing on Debian, so cAdvisor does not collect the relevant data.

The solution simply consists in adding the line:
```
GRUB_CMDLINE_LINUX="cgroup_enable=memory"
```
to the file /etc/default/grub. Then, one has to run: sudo update-grub2 and reboot.
