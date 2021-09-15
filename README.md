# Raspibolt_SSH_TOR_Hidden_Service
How to configure SSH access as a TOR hidden service


-Add the following three lines in the section for “location-hidden services” in the torrc file:

$ sudo nano /etc/tor/torrc

> ############### This section is just for location-hidden services ###

> HiddenServiceDir /var/lib/tor/hidden_service_ssh/
> 
> HiddenServiceVersion 3
> 
> HiddenServicePort 22 127.0.0.1:22

-Restart Tor and get your connection address.

$ sudo systemctl restart tor
$ sudo cat /var/lib/tor/hidden_service_ssh/hostname
> gwdllz5g7vky2q4gr45zGuvopjzf33czreca3a3exosftx72ekppkuqd.onion
