This is a simple script designed by reddit user /u/hapticpilot to make it very hard for third parties to link
your morelo transactions to you via your IP address. This script achieves this
extra privacy by sending your morelo transaction to the morelo network via the
Tor network.
&nbsp;

How it works is simple: you pass a raw_morelo_tx file (a morelo transaction
created by morelo-wallet-cli) to this script as an argument and it will
submit this transaction to a morelod, tor onion node via the Tor network. Your
real IP address will be concealed from the remote morelod. The real IP address
of the remote morelod will be concealed from you. Any computers passively
monitoring your connection will not be able to tell which computer you are
connecting to and what data you're sending.
&nbsp;

To make morelo-wallet-cli (the most popular Morelo wallet) create a
raw_morelo_tx file instead of submitting a transaction directly to the
morelo network via your Internet connection, you have to start
morelo-wallet-cli with the --do-not-relay switch or add do-not-relay=1
to your morelo-wallet-cli configuration file.
&nbsp;

Make sure you have installed Tor before attempting to use this script.
&nbsp;

https://www.torproject.org/
&nbsp;

If you use the default tor settings, this script should connect to your local
tor node without issue.
&nbsp;
 
You should inspect and if necessary edit the USER CONFIG variables in this
script before using it.

## Instructions

This script should work on every GNU/Linux system. I expect it will work on Mac OS X & even Windows 10 if you install their linuxy compatibility stuff.
&nbsp;

To use the script:

1. Make sure tor, bash and curl are installed on your system.
2. Save the script to a file named something like: submit-morelo-tx.sh
3. Make the script executable: chmod a+x submit-morelo-tx.sh
4. Read the script to learn how to use it and to check that it doesn't do something evil (you shouldn't trust me: I'm a stranger from the Internet).
5. When you're ready, usage is as simple as: ./submit-morelo-tx.sh raw_morelo_tx

Done!
