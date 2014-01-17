# QR Code

[![Scrutinizer Quality Score](https://scrutinizer-ci.com/g/pH-7/QRCode-Generator-PHP-Class/badges/quality-score.png?s=e469a64a9ac43a7b4233f5813a7078b08a5b6956)](https://scrutinizer-ci.com/g/pH-7/QRCode-Generator-PHP-Class/)

## Description

This **QRCode PHP class** allows you to easily generate a simple **QR code** using **vCard** 4.0 and the Google Chart API.

Here also two video explanation of QR code: http://www.youtube.com/watch?v=B3lrcOhmp9g and http://www.youtube.com/watch?v=IphTJHiKGos


## How to Use

Here's a basic example:

```php
<?php

require 'QRCode.class.php'; // Include the QRCode class

/**
 * If you have PHP 5.4 or higher, you can instantiate the object like this:
 * (new QRCode)->fullName('...')->... // Create vCard Object
 */
$oQRC = new QRCode; // Create vCard Object
$oQRC->fullName('Pierre-Henry Soria') // Add Full Name
    ->nickName('PH7') // Add Nickname
    ->gender('M') // Add Gender
    ->email('ph7software@gmail.com') // Add Email Address
    ->impp('phs_7@aol.com') // Add Instant Messenger
    ->url('http://ph-7.github.com') // Add URL Website
    ->note('Hello to all! I am a web developer. As hobbit, I like climbing and swimming ...') // Add Note
    ->categories('developer,designer,climber,swimmer') // Add Categories
    ->photo('http://files.phpclasses.org/picture/user/1122955.jpg') // Add Avatar
    ->lang('en-US') // Add Language
    ->finish(); // End vCard

// echo '<p><img src="' . $oQRC->get(300) . '" alt="QR Code" /></p>'; // Generate and display the QR Code
$oQRC->display(); // Display
```

You also have a sample file here: http://github.com/pH-7/QRCode-Generator-PHP-Class/blob/master/example.php


## Server Requirements

PHP 5.2.4 or higher.


## Author

Pierre-Henry Soria


## Contact

Contact me at: *ph7software [at] gmail.com*


## License

[General Public License 3](http://www.gnu.org/licenses/gpl.html) or later; See the LICENSE.txt file.
