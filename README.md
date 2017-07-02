# ssh-revtun: SSH reverse tunnel

You would like to ssh into a machine behind a firewall? Then you can use this
handy little script which connects out from your firewalled machine A to a
remote machine B. You can then connect via the remote machine B to machine A on
a custom tunnel.

# Remote configuration

On the remote machine B you can connect to machine A:

    $ ssh user@localhost -p 1234

# Tips & tricks

To surf on `machineA` via a socks5 `machineC` which has a reverse-tunnel setup to `machineB`

    machineA$ ssh -L 8888:localhost:8888 machineB "ssh -D 8888 machineC"
>>>>>>> 7ffc664ba68941486c464f452d0f40ef14904be3
