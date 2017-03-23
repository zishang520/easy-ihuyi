# easy-ihuyi

[![Packagist](https://img.shields.io/packagist/l/zhenggg/easy-ihuyi.svg?maxAge=2592000)](https://packagist.org/packages/zhenggg/easy-ihuyi)
[![Total Downloads](https://img.shields.io/packagist/dt/zhenggg/easy-ihuyi.svg?style=flat-square)](https://packagist.org/packages/zhenggg/easy-ihuyi)

<p>:calling: The best ihuyi composer package.</p>

# Requirement

- PHP >= 5.6

# Installation

```shell
$ composer require "zhengg/easy-ihuyi"
```

# Usage

```php
use Zhenggg\Huyi\EasyHuyi;
$config = [
    'APIID' => 'xxx',
    'APIKEY' => 'xxx',
];
/**
 *  $phone_number 多个号码以英文,隔开
 */
$easySms = new EasyHuyi($config);
//短信验证码/通知
$easySms->sms()->content($content)->send($phone_number);
//语音验证码
$easySms->voice()->content($content)->send($phone_number);
//国际短信
$easySms->isms()->content($content)->send($phone_number);
//短信营销
$easySms->yxsms()->content($content)->send($phone_number);
//彩信营销(定时发送) 
$easySms->yxsms()->content($content)->stime($time)->send($phone_number);
//彩信营销
$easySms->mms()->mmsid($mmsid)->pid($pid)->send($phone_number);
```
# License

MIT
