# CSS Flip

[![Build Status](https://travis-ci.org/Penobit/css-flip.svg?branch=master)](https://travis-ci.org/Penobit/css-flip) [![Latest Stable Version](https://img.shields.io/packagist/v/Penobit/css-flip.svg)](https://packagist.org/packages/penobit/css-flip) [![Total Downloads](https://img.shields.io/packagist/dt/Penobit/css-flip.svg)](https://packagist.org/packages/penobit/css-flip) [![Downloads Month](https://img.shields.io/packagist/dm/Penobit/css-flip.svg)](https://packagist.org/packages/penobit/css-flip) [![Petreon donation](https://img.shields.io/badge/patreon-donate-orange.svg)](https://www.patreon.com/penobit) [![PayPal donation](https://img.shields.io/badge/paypal-donate-blue.svg)](https://paypal.me/penobit)

 Flip css/scss direction from ltr to rtl or rtl to ltr with single line php code!

---

 - [Installation](#installation)
 - [Usage](#usage)
## Installation

Install this package via [Composer](https://getcomposer.org/).

```
composer require penobit/css-flip
```

You can also download latest release from Github and include `src/CSSFlip.php` manually but i recommend using composer to stay up to date and easier install and usage

## Usage

Create CSSFlip object

```php
use Penobit\CSSFlip\CSSFlip;

$cssFlip = new CSSFlip();
$cssCode = <<<CSS
body{
  direction: ltr;
}
div{
  text-align:left;
  margin-left: 20px;
  margin-right: 2rem;
}
span{
  padding: 10px 15px 20px 25px;
}
CSS;

$flippedCssCode = $cssFlip->transform($cssCode);

/* 
# Output of above code will be
body{
  direction: rtl;
}
div{
  text-align:right;
  margin-right: 20px;
  margin-left: 2rem;
}
span{
  padding: 10px 15px 20px 25px;
  padding: 10px 25px 20px 15px;
}
*/
```
