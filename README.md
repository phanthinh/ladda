ladda
=====

ladda directive



## Requirements

 - AngularJS v1.2.4+

## Installing

Add js inline 
```html
	<script src="js/libs/ladda/spin.min.js"></script>	
	<script src="js/libs/ladda/ladda.min.js"></script>
	
	<link rel="stylesheet" href="css/libs/ladda/ladda-themeless.min.css">	


## Example
```html
<script src="js/libs/angular/angular.min.js"></script>

<script>
    var test = angular.module('MyModule', [
	'masonry'
]);
test.directive("ladda", ["$compile", function(a) {
	return {
		restrict: "A",
		link: function(b, c, d) {
			c.addClass("ladda-button"), angular.isUndefined(c.attr("data-style")) && c.attr("data-style", "zoom-out");
			var e = Ladda.create(c[0]);
			a(angular.element(c.children()[0]).contents())(b), b.$watch(d.ladda, function(a) {
				a || angular.isNumber(a) ? (e.isLoading() || e.start(), angular.isNumber(a) && e.setProgress(a)) : e.stop()
			})
		}
	}
}]);





</script>


