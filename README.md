Laravel PredictionIO
====================

*Based on [endroid](http://endroid.nl/)*


The Laravel PredictionIO library provides a client which offers easy access to a PredictionIO recommendation engine.
PredictionIO is an open source machine learning server for software developers to create predictive features, such as
personalization, recommendation and content discovery.

Through a small set of simple calls, all server functionality is exposed to your application. You can add users and items,
register actions between these users and items and retrieve recommendations deduced from this information by any
[`PredictionIO`](http://prediction.io/) recommendation engine. Applications range from showing recommended products in a
web shop to discovering relevant experts in a social collaboration network.


## Installation
Add "bratao/prediction-io": "1.*@dev" to composer.json.

Add 'Bratao\PredictionIO\PredictionServiceProvider' and 
'Prediction'      => 'Bratao\PredictionIO\Facade', to app.php
 
## Usage

```php
<?php

// populate with users, items and actions
Predict::createItem($itemId);
Predict::recordAction($userId, $itemId, 'view');

// get recommendations and similar items
$recommendations = Predict::getRecommendations($userId, $engine, $count);
$similarItems = Predict::getSimilarItems($itemId, $engine, $count);

```

## License

This bundle is under the MIT license. For the full copyright and license information, please view the LICENSE file that
was distributed with this source code.
