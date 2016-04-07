Home Base fstab restore script
==============================
This is just a startup script I wrote for the Linux machine at work (running
Mint/Ubuntu).  I'm not sure why (and I hate that), but we often plug in drives
via SATA and unplug them later, and the OS automatically adds fstab entries for
these drives and ends up looking for them on future boots.  I wrote this script
to run at every startup and shutdown to just replace /etc/fstab with a clean
copy.  It's not the best solution, but it works and it's out of our way.

To set this up on a clean install, make sure that /etc/fstab is set up as you
want it.  Then, run `sudo ./hb-restore-fstab install`.  This will make a copy
of /etc/fstab at /etc/fstab-clean and install the script into rc.d.
