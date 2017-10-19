In order to run this script you would require to have a working Bitcoin Core Daemon running and updated.

#1 Import file.sql, after reading #3

#2 Set correct database infos in connection.php and desired parameters in btc.php

#3 Set RPC Bitcoind server credentials in *.sql file before upload.

#4 Create main wallet in bitcoind :
./bitcoin-cli getaccountaddress main
*Note: It is important that wallet keeps default name wich is: main

#5 Encrypt the wallet

./bitcoin-cli encryptwallet "inputpass"
then set in *.sql file on LINE37 

#6 To change password
./bitcoin-cli walletpassphrasechange "oldpass" "newpass"
*Note: Do not forget to update also in *.sql

#7 Set cron job to processcashout.php (time recommended is 5-10 minutes) so each X minutes script runs and process all transactions.
*Note: Please google about cron jobs for your desired OS.

#8.Semi-Mini-Admin Panel
to login = /bengamipapai38o.php?login=$walletpass (the value you set)


Enjoy! Please try to make the world a better place.





"It's easy to do harm, but hard to do good; be different and take the hard part"
