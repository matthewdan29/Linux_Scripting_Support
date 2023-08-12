	When adding a new or customized service to a Linux SysVinit server, you must complete three steps in order to have the service managed by SysVint. 

		1) Create a new or customized service script file. 
		2) Move the new or customized service script to the propter location for SysVinit management. 
		3) Add the service to a speicfic runlevel. 


/* One line you should be sure to check out and possibly modify in your new script is the chkconfig line that is commented out 

		chkconfig: 2345 25 10 

 * When you add the service script in a later step, the chkconfig command reads that line to set runlevels at which the service starts (2, 3, 4, and 5), its run order when the script is set to start (25), and its kill order when it is set to stop (10) */

	2) Next move the newly made script to the proper place with the command 
		$cp Example_script_cup /etc/rc.d/init.d 

	3) Add the service to runlevel dir
		# chkconfig --add Example_script_cup 
		# ls /etc/rc?.d/*Example_script_cup

		After that use the service command to start/stop then reboot 


Hey change the script to sh 