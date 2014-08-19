Ionic Contrib: Swipeable Cards
===================

Swipeable card based layout for Ionic and Angular. As seen in apps like [Jelly](http://jelly.co/)

[Demo](http://ionicframework.com/demos/swipe-cards/)

## Usage

Include `ionic.swipecards.js` after the rest of your Ionic and Angular includes. Then use the following AngularJS directives:

```html
<swipe-cards>
  <swipe-card ng-repeat="card in cards" on-destroy="cardDestroyed($index)" on-card-swipe-left="cardSwiped($index)" on-card-swipe-right="cardSwiped($index)">
    Card content here
  </swipe-card>
</swipe-cards>
```

To add new cards dynamically, just add them to the cards array:

```javascript
$scope.cards = [
  { // card 1 },
  { // card 2 }
];

$scope.cardDestroyed = function(index) {
  $scope.cards.splice(index, 1);
};

$scope.cardSwiped = function(index) {
  var newCard = // new card data
  $scope.cards.push(newCard);
};
```

To lock swiping use lock-x or lock-y, and enable-flip to allow tapping to flip the card

<swipe-card lock-x="true" enable-flip="true">
    Card content here
</swipe-card>

