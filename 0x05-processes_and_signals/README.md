Tasks 0. What is my PID mandatory Write a Bash script that displays its own PID.

sylvain@ubuntu$ ./0-what-is-my-pid 4120 sylvain@ubuntu$ Repo:

GitHub repository: alx-system_engineering-devops Directory: 0x05-processes_and_signals File: 0-what-is-my-pid

List your processes mandatory Write a Bash script that displays a list of currently running processes.
Requirements:

Must show all processes, for all users, including those which might not have a TTY Display in a user-oriented format Show process hierarchy sylvain@ubuntu$ ./1-list_your_processes | head -50 USER PID %CPU %MEM VSZ RSS TTY STAT START TIME COMMAND root 2 0.0 0.0 0 0 ? S Feb13 0:00 [kthreadd] root 3 0.0 0.0 0 0 ? S Feb13 0:00 _ [ksoftirqd/0] root 4 0.0 0.0 0 0 ? S Feb13 0:00 _ [kworker/0:0] root 5 0.0 0.0 0 0 ? S< Feb13 0:00 _ [kworker/0:0H] root 7 0.0 0.0 0 0 ? S Feb13 0:02 _ [rcu_sched] root 8 0.0 0.0 0 0 ? S Feb13 0:03 _ [rcuos/0] root 9 0.0 0.0 0 0 ? S Feb13 0:00 _ [rcu_bh] root 10 0.0 0.0 0 0 ? S Feb13 0:00 _ [rcuob/0] root 11 0.0 0.0 0 0 ? S Feb13 0:00 _ [migration/0] root 12 0.0 0.0 0 0 ? S Feb13 0:02 _ [watchdog/0] root 13 0.0 0.0 0 0 ? S< Feb13 0:00 _ [khelper] root 14 0.0 0.0 0 0 ? S Feb13 0:00 _ [kdevtmpfs] root 15 0.0 0.0 0 0 ? S< Feb13 0:00 _ [netns] root 16 0.0 0.0 0 0 ? S< Feb13 0:00 _ [writeback] root 17 0.0 0.0 0 0 ? S< Feb13 0:00 _ [kintegrityd] root 18 0.0 0.0 0 0 ? S< Feb13 0:00 _ [bioset] root 19 0.0 0.0 0 0 ? S< Feb13 0:00 _ [kworker/u3:0] root 20 0.0 0.0 0 0 ? S< Feb13 0:00 _ [kblockd] root 21 0.0 0.0 0 0 ? S< Feb13 0:00 _ [ata_sff] root 22 0.0 0.0 0 0 ? S Feb13 0:00 _ [khubd] root 23 0.0 0.0 0 0 ? S< Feb13 0:00 _ [md] root 24 0.0 0.0 0 0 ? S< Feb13 0:00 _ [devfreq_wq] root 25 0.0 0.0 0 0 ? S Feb13 0:41 _ [kworker/0:1] root 27 0.0 0.0 0 0 ? S Feb13 0:00 _ [khungtaskd] root 28 0.0 0.0 0 0 ? S Feb13 0:00 _ [kswapd0] root 29 0.0 0.0 0 0 ? S< Feb13 0:00 _ [vmstat] root 30 0.0 0.0 0 0 ? SN Feb13 0:00 _ [ksmd] root 31 0.0 0.0 0 0 ? S Feb13 0:00 _ [fsnotify_mark] root 32 0.0 0.0 0 0 ? S Feb13 0:00 _ [ecryptfs-kthrea] root 33 0.0 0.0 0 0 ? S< Feb13 0:00 _ [crypto] root 45 0.0 0.0 0 0 ? S< Feb13 0:00 _ [kthrotld] root 46 0.0 0.0 0 0 ? S Feb13 0:00 _ [kworker/u2:1] root 65 0.0 0.0 0 0 ? S< Feb13 0:00 _ [deferwq] root 66 0.0 0.0 0 0 ? S< Feb13 0:00 _ [charger_manager] root 108 0.0 0.0 0 0 ? S< Feb13 0:00 _ [kpsmoused] root 125 0.0 0.0 0 0 ? S Feb13 0:00 _ [scsi_eh_0] root 126 0.0 0.0 0 0 ? S Feb13 0:00 _ [kworker/u2:2] root 172 0.0 0.0 0 0 ? S Feb13 0:00 _ [jbd2/sda1-8] root 173 0.0 0.0 0 0 ? S< Feb13 0:00 _ [ext4-rsv-conver] root 409 0.0 0.0 0 0 ? S< Feb13 0:00 _ [iprt] root 549 0.0 0.0 0 0 ? S< Feb13 0:00 _ [kworker/u3:1] root 808 0.0 0.0 0 0 ? S Feb13 0:00 _ [kauditd] root 834 0.0 0.0 0 0 ? S< Feb13 0:00 _ [rpciod] root 846 0.0 0.0 0 0 ? S< Feb13 0:00 _ [nfsiod] root 1 0.0 0.4 33608 2168 ? Ss Feb13 0:00 /sbin/init root 373 0.0 0.0 19472 408 ? S Feb13 0:00 upstart-udev-bridge --daemon root 378 0.0 0.2 49904 1088 ? Ss Feb13 0:00 /lib/systemd/systemd-udevd --daemon root 518 0.0 0.1 23416 644 ? Ss Feb13 0:00 rpcbind statd 547 0.0 0.1 21536 852 ? Ss Feb13 0:00 rpc.statd -L sylvain@ubuntu$ Repo:

GitHub repository: alx-system_engineering-devops Directory: 0x05-processes_and_signals File: 1-list_your_processes

Show your Bash PID mandatory Using your previous exercise command, write a Bash script that displays lines containing the bash word, thus allowing you to easily get the PID of your Bash process.
Requirements:

You cannot use pgrep The third line of your script must be # shellcheck disable=SC2009 (for more info about ignoring shellcheck error here) sylvain@ubuntu$ sylvain@ubuntu$ ./2-show_your_bash_pid sylvain 4404 0.0 0.7 21432 4000 pts/0 Ss 03:32 0:00 _ -bash sylvain 4477 0.0 0.2 11120 1352 pts/0 S+ 03:40 0:00 _ bash ./2-show_your_bash_PID sylvain 4479 0.0 0.1 10460 912 pts/0 S+ 03:40 0:00 _ grep bash sylvain@ubuntu$ Here we can see that my Bash PID is 4404.

Repo:

GitHub repository: alx-system_engineering-devops Directory: 0x05-processes_and_signals File: 2-show_your_bash_pid

Show your Bash PID made easy mandatory Write a Bash script that displays the PID, along with the process name, of processes whose name contain the word bash.
Requirements:

You cannot use ps sylvain@ubuntu$ ./3-show_your_bash_pid_made_easy 4404 bash 4555 bash sylvain@ubuntu$ ./3-show_your_bash_pid_made_easy 4404 bash 4557 bash sylvain@ubuntu$ Here we can see that:

For the first iteration: bash PID is 4404 and that the 3-show_your_bash_pid_made_easy script PID is 4555 For the second iteration: bash PID is 4404 and that the 3-show_your_bash_pid_made_easy script PID is 4557 Repo:

GitHub repository: alx-system_engineering-devops Directory: 0x05-processes_and_signals File: 3-show_your_bash_pid_made_easy

To infinity and beyond mandatory Write a Bash script that displays To infinity and beyond indefinitely.
Requirements:

In between each iteration of the loop, add a sleep 2 sylvain@ubuntu$ ./4-to_infinity_and_beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond ^C sylvain@ubuntu$ Note that I ctrl+c (killed) the Bash script in the example.

Repo:

GitHub repository: alx-system_engineering-devops Directory: 0x05-processes_and_signals File: 4-to_infinity_and_beyond

Don't stop me now! mandatory We stopped our 4-to_infinity_and_beyond process using ctrl+c in the previous task, there is actually another way to do this.
Write a Bash script that stops 4-to_infinity_and_beyond process.

Requirements:

You must use kill Terminal #0

sylvain@ubuntu$ ./4-to_infinity_and_beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond Terminated sylvain@ubuntu$ Terminal #1

sylvain@ubuntu$ ./5-dont_stop_me_now sylvain@ubuntu$ I opened 2 terminals in this example, started by running my 4-to_infinity_and_beyond Bash script in terminal #0 and then moved on terminal #1 to run 5-dont_stop_me_now. We can then see in terminal #0 that my process has been terminated.

Repo:

GitHub repository: alx-system_engineering-devops Directory: 0x05-processes_and_signals File: 5-dont_stop_me_now

Stop me if you can mandatory Write a Bash script that stops 4-to_infinity_and_beyond process.
Requirements:

You cannot use kill or killall Terminal #0

sylvain@ubuntu$ ./4-to_infinity_and_beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond Terminated sylvain@ubuntu$ Terminal #1

sylvain@ubuntu$ ./6-stop_me_if_you_can sylvain@ubuntu$ I opened 2 terminals in this example, started by running my 4-to_infinity_and_beyond Bash script in terminal #0 and then moved on terminal #1 to run 6-stop_me_if_you_can. We can then see in terminal #0 that my process has been terminated.

Repo:

GitHub repository: alx-system_engineering-devops Directory: 0x05-processes_and_signals File: 6-stop_me_if_you_can

Highlander mandatory Write a Bash script that displays:
To infinity and beyond indefinitely With a sleep 2 in between each iteration I am invincible!!! when receiving a SIGTERM signal Make a copy of your 6-stop_me_if_you_can script, name it 67-stop_me_if_you_can, that kills the 7-highlander process instead of the 4-to_infinity_and_beyond one.

Terminal #0

sylvain@ubuntu$ ./7-highlander To infinity and beyond To infinity and beyond I am invincible!!! To infinity and beyond I am invincible!!! To infinity and beyond To infinity and beyond To infinity and beyond I am invincible!!! To infinity and beyond ^C sylvain@ubuntu$ Terminal #1

sylvain@ubuntu$ ./67-stop_me_if_you_can sylvain@ubuntu$ ./67-stop_me_if_you_can sylvain@ubuntu$ ./67-stop_me_if_you_can sylvain@ubuntu$ I started 7-highlander in Terminal #0 and then run 67-stop_me_if_you_can in terminal #1, for every iteration we can see I am invincible!!! appearing in terminal #0.

Repo:

GitHub repository: alx-system_engineering-devops Directory: 0x05-processes_and_signals File: 7-highlander

Beheaded process mandatory Write a Bash script that kills the process 7-highlander.
Terminal #0

sylvain@ubuntu$ ./7-highlander To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond Killed sylvain@ubuntu$ Terminal #1

sylvain@ubuntu$ ./8-beheaded_process sylvain@ubuntu$ I started 7-highlander in Terminal #0 and then run 8-beheaded_process in terminal #1 and we can see that the 7-highlander has been killed.

Repo:

GitHub repository: alx-system_engineering-devops Directory: 0x05-processes_and_signals File: 8-beheaded_process

Process and PID file #advanced Write a Bash script that:
Creates the file /var/run/myscript.pid containing its PID Displays To infinity and beyond indefinitely Displays I hate the kill command when receiving a SIGTERM signal Displays Y U no love me?! when receiving a SIGINT signal Deletes the file /var/run/myscript.pid and terminates itself when receiving a SIGQUIT or SIGTERM signal

sylvain@ubuntu$ sudo ./100-process_and_pid_file To infinity and beyond To infinity and beyond ^CY U no love me?! Executing the 100-process_and_pid_file script and killing it with ctrl+c.

Terminal #0

sylvain@ubuntu$ sudo ./100-process_and_pid_file To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond To infinity and beyond I hate the kill command sylvain@ubuntu$ Terminal #1

sylvain@ubuntu$ sudo pkill -f 100-process_and_pid_file sylvain@ubuntu$ Starting 100-process_and_pid_file in the terminal #0 and then killing it in the terminal #1.

Repo:

GitHub repository: alx-system_engineering-devops Directory: 0x05-processes_and_signals File: 100-process_and_pid_file

Manage my process #advanced
Read:

& init.d Daemon Positional parameters man: sudo

Programs that are detached from the terminal and running in the background are called daemons or processes, need to be managed. The general minimum set of instructions is: start, restart and stop. The most popular way of doing so on Unix system is to use the init scripts.

Write a manage_my_process Bash script that:

Indefinitely writes I am alive! to the file /tmp/my_process In between every I am alive! message, the program should pause for 2 seconds Write Bash (init) script 101-manage_my_process that manages manage_my_process. (both files need to be pushed to git)

Requirements:

When passing the argument start: Starts manage_my_process Creates a file containing its PID in /var/run/my_process.pid Displays manage_my_process started When passing the argument stop: Stops manage_my_process Deletes the file /var/run/my_process.pid Displays manage_my_process stopped When passing the argument restart Stops manage_my_process Deletes the file /var/run/my_process.pid Starts manage_my_process Creates a file containing its PID in /var/run/my_process.pid Displays manage_my_process restarted Displays Usage: manage_my_process {start|stop|restart} if any other argument or no argument is passed Note that this init script is far from being perfect (but good enough for the sake of manipulating process and PID file), for example we do not handle the case where we check if a process is already running when doing ./101-manage_my_process start, in our case it will simply create a new process instead of saying that it is already started.

sylvain@ubuntu$ sudo ./101-manage_my_process Usage: manage_my_process {start|stop|restart} sylvain@ubuntu$ sudo ./101-manage_my_process start manage_my_process started sylvain@ubuntu$ tail -f -n0 /tmp/my_process I am alive! I am alive! I am alive! I am alive! ^C sylvain@ubuntu$ sudo ./101-manage_my_process stop manage_my_process stopped sylvain@ubuntu$ cat /var/run/my_process.pid cat: /var/run/my_process.pid: No such file or directory sylvain@ubuntu$ tail -f -n0 /tmp/my_process ^C sylvain@ubuntu$ sudo ./101-manage_my_process start manage_my_process started sylvain@ubuntu$ cat /var/run/my_process.pid 11864 sylvain@ubuntu$ sudo ./101-manage_my_process restart manage_my_process restarted sylvain@ubuntu$ cat /var/run/my_process.pid 11918 sylvain@ubuntu$ tail -f -n0 /tmp/my_process I am alive! I am alive! I am alive! ^C sylvain@ubuntu$ Repo:

GitHub repository: alx-system_engineering-devops Directory: 0x05-processes_and_signals File: 101-manage_my_process, manage_my_process

Zombie #advanced
Read what a zombie process is.

Write a C program that creates 5 zombie processes.

Requirements:

For every zombie process created, it displays Zombie process created, PID: ZOMBIE_PID Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl When your code is done creating the parent process and the zombies, use the function bellow int infinite_while(void) { while (1) { sleep(1); } return (0); } Example:

Terminal #0

sylvain@ubuntu$ gcc 102-zombie.c -o zombie sylvain@ubuntu$ ./zombie Zombie process created, PID: 13527 Zombie process created, PID: 13528 Zombie process created, PID: 13529 Zombie process created, PID: 13530 Zombie process created, PID: 13531 ^C sylvain@ubuntu$ Terminal #1

sylvain@ubuntu$ ps aux | grep -e 'Z+.' sylvain 13527 0.0 0.0 0 0 pts/0 Z+ 01:19 0:00 [zombie] sylvain 13528 0.0 0.0 0 0 pts/0 Z+ 01:19 0:00 [zombie] sylvain 13529 0.0 0.0 0 0 pts/0 Z+ 01:19 0:00 [zombie] sylvain 13530 0.0 0.0 0 0 pts/0 Z+ 01:19 0:00 [zombie] sylvain 13531 0.0 0.0 0 0 pts/0 Z+ 01:19 0:00 [zombie] sylvain 13533 0.0 0.1 10460 964 pts/2 S+ 01:19 0:00 grep --color=auto -e Z+. sylvain@ubuntu$ In Terminal #0, I start by compiling 102-zombie.c and executing zombie which creates 5 zombie processes. In Terminal #1, I display the list of processes and look for lines containing Z+.* which catches zombie process.

Repo:

GitHub repository: alx-system_engineering-devops Directory: 0x05-processes_and_signals File: 102-zombie.c
