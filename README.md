# grphp-statsd - StatsD interceptor for grphp

StatsD interceptor for measuring [grphp](https://github.com/bigcommerce/grphp) client requests.

## Installation

```bash
composer require bigcommerce/grphp-statsd
```

## Configuration

```php
$config = [
    'host' => 'my.statsd.service',
    'port' => 8125,
    
    // optional config options
    'namespace' => 'myapp',
    'sample_rate' => 1.0, // 0->1.0 scale. 1.0 is all requests.
    'mtu' => 1500, // MTU rate
    'persistent' => false, // keep connection persistent
    'timeout' => 600, // in seconds
    'tcp' => false, // true uses TCP instead of UDP
];
$client->addInterceptor(new \Grphp\StatsD\Interceptor($config));
```

## License

Copyright (c) 2017-present, BigCommerce Pty. Ltd. All rights reserved 

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated 
documentation files (the "Software"), to deal in the Software without restriction, including without limitation the 
rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit 
persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the 
Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE 
WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR 
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR 
OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
