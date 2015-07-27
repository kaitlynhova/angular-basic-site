#How to run the project

Pull down the project and run a [MAMP](https://www.mamp.info/en/) server on the folder. 
The project should be visible at http://localhost:8888/ on your computer.

#How to add faq page/tab (PHU example)

###in ** routes.js ** add: 
```
$routeProvider.when('/phu', {
  templateUrl: 'partials/phu-partial.html',
  controller: ‘phuCTL'
});
```

###in **controllers.js** add
```
.controller(‘phuCTL', function(){

})
```

###Add this to **home-partial.html**
```
  <!-- ROW ITEM -->
  <div class="row faq-item" ng-class="{active: isActive('/phu')}">
    <div class="col-xs-10"> <p class="list-title">Why is phu so awesome?</p></div>
    <div class="col-xs-2">
      <a href="#/phu">
        <img class="arrow" src="img/angle-right.svg">
      </a>
    </div>
  </div>
  <!-- /ROW ITEM-->
```
###Add this new file to Partials folder:


phu-partial.html

^^in this file, you can copy any other "what-evs-partial.html" and replace with whatever code you want

