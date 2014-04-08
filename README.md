php_mailcatcher
===============

### How to install

Copy the file `phpsendmail` to your system, e.g to `/usr/local/bin/phpsendmail`.

Now configure PHP to use the Mailcatcher. Open your `php.ini` and change the following line (and restart Apache afterwards):

`sendmail_path = /usr/local/bin/phpsendmail`

Now every Mail that is sent by PHP will be written to `/tmp/phpmail/`.

### Configuration

If you want to change the Output path, simply open the mailcatcher file and change the following line:

`define('OUTPUT_PATH', '/tmp/phpmail/');`

##### Path to PHP Binary

If your php Binary is not at the default location (/usr/bin/php) you may also need to change the shebang line (first line) of the script:

`#!/usr/bin/php`