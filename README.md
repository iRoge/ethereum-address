```lang=bash
$ composer require iroge/ethereum-address
```

## Usage

Create a new address:

```php
<?php

require_once 'vendor/autoload.php';

use IRoge\Ethereum\Address;

$address = new Address();

// get address
$address->get();
// 4e1c45599f667b4dc3604d69e43722d4ace6b770

$address->getPrivateKey();
// 33eb576d927573cff6ae50a9e09fc60b672a8dafdfbe3045c7f62955fc55ccb4

$address->getPublicKey();
// 20876c03fff2b09ea01861f3b3789ada54a20a8c5e90170618364cbb02d8e6408401e120158f489376a1db3f8cde24f9432976d2f89aeb193fb5becc094a28b9
```

Or load one from private key:

```php
<?php

require_once 'vendor/autoload.php';

use IRoge\Ethereum\Address;

$privateKey = '33eb576d927573cff6ae50a9e09fc60b672a8dafdfbe3045c7f62955fc55ccb4';
$address = new Address($privateKey);

// get address
$address->get();
// 4e1c45599f667b4dc3604d69e43722d4ace6b770

$address->getPrivateKey();
// 33eb576d927573cff6ae50a9e09fc60b672a8dafdfbe3045c7f62955fc55ccb4

$address->getPublicKey();
// 20876c03fff2b09ea01861f3b3789ada54a20a8c5e90170618364cbb02d8e6408401e120158f489376a1db3f8cde24f9432976d2f89aeb193fb5becc094a28b9
```

## License

MIT