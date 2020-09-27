# bssm - Bash Simple Server Monitor

The idea behind this is to enable one to roughly look for their server's status without having to log in.
There are many great monitoring solutions available that will often depend on other software like a PHP server and a database.

What bssm does is to simply write a text file with stats every time it is executed - so usually you would want to use it with a cron job or call it from another script. This text file can then be delivered for example via any basic HTTP server, like the very light webfs.

Therefore, and because bssm uses only tools/commands that are already present on most systems, it should run even on the most minimal machines.

Configuration is done via a separate config file, to keep things simple and have all the options at one glance. By default, all available modules are activated.

The output text file is overwritten every time the script is executed, but it is possible to keep an archive of timestamped output files. This is disabled by default.

It is tested on Debian 10 - on systems with a different package base it can't be ruled out that some of the tools used react slightly different than expected.

Requirements: neofetch, ip (iproute2), various standard tools virtually any system should have. There is no built-in requirements check for performance reasons.

