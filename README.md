angular-range
==============

Slider directive implementation for AngularJS, without jQuery dependencies. Requires AngularJS v1.2.0 or higher (optional isolate scope bindings support).


### Todo:
* redo repo
* remove coffeescript
* add grunt
* add bower



### Example:


    <slider class="slider" floor="100" ceiling="1000" step="50" precision="2" ng-model="item.cost"></slider>

### Range:

    <range class="slider" floor="10" ceiling="60" ng-model-low="position.minAge" ng-model-high="position.maxAge" range-info-title="Time range"></range>

### Formatting:

Raw data can be formatted as text using the _translate_ attribute.
In your controller:

    $scope.currencyFormatting = function(value) { return value.toString() + " $" }

And your HTML:

    <range floor="100" ceiling="1000" step="50" precision="2" ng-model="item.cost" translate="currencyFormatting"></range>

### Usage:

Make sure to load AngularJS first, and then `angular-slider.js`. Also include the related `angular-slider.css`.

The module is named `uiSlider`. To enable it, you must simply list it as a dependency in your app. Example:

    var app = angular.module('app', ['uiSlider', 'ngResource', ...]);

You can then use it in your templates like so:

    <html ng-app='app'>
        ...
        <body>
            ...
            <slider ...></slider>
        </body>
    </html>


### Known issues:

1. When applying filters or orders within an ng-repeat directive, the element can abruptly change its position when the value attached to the slider causes a filter to activate or the order to change.
Example: In the above snippet, it would be a very bad idea to order the list by item.cost.

### Roadmap:

1. ~~Touch events support~~
2. Smooth curve heterogeneity
3. Filters support

### License: MIT
