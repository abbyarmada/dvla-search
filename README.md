# DVLA Search PHP SDK
PHP SDK for DVLASearch API

# Requirements

* PHP >=7.0.0

# Installation

`composer require dvlasearch/sdk`

# Usage

Currently `VehicleSearchClient` is the only class available.

```php
<?php

use DVLASearch\SDK\VehicleSearchClient;

$client = new VehicleSearchClient('API KEY HERE');
$result = $client->get('NUMBER PLATE HERE');
```

Returns on success

```
object(stdClass)#17 (21) {
  ["make"]=> string(10) "VOLKSWAGEN"
  ["dateOfFirstRegistration"]=> string(12) "23 July 2009"
  ["yearOfManufacture"]=> string(4) "2009"
  ["cylinderCapacity"]=> string(6) "1968cc"
  ["co2Emissions"]=> string(8) "167 g/km"
  ["fuelType"]=> string(6) "DIESEL"
  ["taxStatus"]=> string(11) "Tax not due"
  ["colour"]=> string(6) "SILVER"
  ["typeApproval"]=> string(2) "M1"
  ["wheelPlan"]=> string(17) "2 AXLE RIGID BODY"
  ["revenueWeight"]=> string(13) "Not available"
  ["taxDetails"]=> string(24) "Tax due: 01 October 2016"
  ["motDetails"]=> string(22) "Expires: 28 April 2017"
  ["taxed"]=> bool(true)
  ["mot"]=> bool(true)
  ["vin"]=> string(17) "WVGZZZ5NZAW007903"
  ["model"]=> string(6) "Tiguan"
  ["transmission"]=> string(6) "Manual"
  ["numberOfDoors"]=> string(1) "5"
  ["sixMonthRate"]=> string(0) ""
  ["twelveMonthRate"]=> string(0) ""
}
```

Returns on error

```
object(stdClass)#17 (2) {
  ["message"]=> string(15) "API key invalid"
  ["error"]=> int(1)
}
```
