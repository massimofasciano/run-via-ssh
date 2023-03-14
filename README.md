# run-via-ssh
A simple shell script to run a command on a remote ssh host.

First argument is the SSH remote (user@host).
Second argument is the program to run.
The rest are arguments for the program.

I use it to test cross-compiled builds on raspberry pi by adding a runner field in ~/.cargo/config
```
[target.armv7-unknown-linux-gnueabihf]
linker = "arm-linux-gnueabihf-gcc"
runner = ["run-via-ssh", "pi@raspberry.local"]
```
