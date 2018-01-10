Welcome to the AngularJS-UI wiki!


https://angular-ui.github.io/bootstrap/
https://docs.angularjs.org/api/ng/filter/date

## angular ui bootstrap:

* datepicker
* Timepicker
* Typehead
**  Rating->    allow user to give rating
* collapse and Accordion  ->show and hide pop-up
* popover and Tooltip

## Remaining ui BOOTSTRAP:

* ->ALERT,BUTTONS,CAROUSELS
* ->Dropdowns,pagination,progressBar and Tabs


### datepicker:

* min-date
* show-weeks
* min-height


`var angularFormApp = angular.module('angularFormApp',["ngRoute","ui.bootstrap"]);`


`<div class="form-group">`
`<label for="dateHired" class="col-sm-3 control-label">Date Hired</label>`
`<div class="col-sm-9">`
`<datepicker name="dateHired" ng-model="editableEmployee.dateHired">`
`</datepicker>`
`</div>`
`</div>`

### TimePicker:

* ng-model
* hour-step
* minutes-step
* show-meridian
* meridians
* readonly-input



`<div class="form-group">`
`<label for="breakTime" class="col-sm-3 control-label">Date Hired</label>`
`<div class="col-sm-9">`
`<timepicker name="breakTime" ng-model="editableEmployee.dateHired">`
`</timepicker>`
`</div>`
`</div>`

### Typehead directive:

### ng-model:

`<input type="text" ng-model="selected"  typehead="state for state in states | filter:$viewValue | limitTo:8" class="form-control">`
`<input type="text" ng-model="asyncSelected"  typehead="state for state in states | filter:$viewValue | limitTo:8" class="form-control">`


`<input type="text" id="topProramming" name="topProgrammingLanuage" `
`ng-model= "editableEmployee.topProgrammingLanguage"`
  `typehead="language for language in programmingLnguage | filter:$viewValue | limitTo:8" class="form-control">`
--------------
`typehead =" language for language in programmingLanguage | filter:$viewValue/"`

### controller.js:


`$scope.programmingLangauges = [`
`"c",`
`"c+",`
`"javascript",`
`"java",`
`"pascal",`
`"perl",`
`"php"`
`];`


### Rating:

* ng-model
* max
* readonly
* on-leave
* state-on
* state-off
* rating-states

* rating--->element:


`<rating ng-model="rate" >`

`<div class="form-group">`
`<label for="interviewRating" class="col-sm-3 control-label">Interview Rating</label>`
`<div class="col-sm-9">`
`<rating id="interviewRating" name="interviewRating"`
`ng-model="interviewRating" max="10"/>`
`</div>`
`</div>`


### collapse:

`<div class="col-sm-offset-3 col-sm-9">`
`<div class="checkbox">`
`<label>`
`<input type="checkbox" value="isunder" ng-model="editableEmployee.isunderNoncompete" />`
`is employee under a non-compete?`
`</label></div></div>`

`<label for="nonCompeteNotes" class="com-sm-3 control-label">`
`non-compete notes`
`</label>`

`<div class="form-group" collapse="!model="editableEmployee.isunderNoncompete" >`
`<label for="noncompeteNotes" class="col-sm-3 control-label">`
`non-compete`
`</label>`
`</label>`



### pop-over:

### tool-tip:

* alert-->

* buttons-->radio,checkbox

* carousel-->dropdown

* pagination-->

* progressBar

tabs-->

### alert:

* onclick()
* close()

### buttons:

* single
* checkbox
* radio

`<button type="button" class="btn btn-primary" ng-model="singlemodel"`
`btn-checkbox btn-checkbox-true="1"  btn-checkbox btn-checkbox-false="0">`

`<label class="btn btn-primary" ng-model="checkbox.left" btn-checkbox>left</label>`
`<label class="btn btn-primary" ng-model="radioModel" btn-radio="'left'">Left</label>`

### carousel:

### <carousel interval="myInterval">
### <slide ng-repeat="slide in slides" active="slide.active">

* dropdown:
* pagination:
* progressbar:
* Tabs:

### AngularJS Form:

-->### required and ngrequired:

### novalidate->to shut the default browser validate

`<input type="text" id="fullname" name="fullname" class="form-control"`
`ng-model="editableEmployee.fullName" ng-required="shouldShowFullName"\>`
`<span ng-show="employeeForm.fullName.$error.required">full name is requires</span>`

### controller.js:

`$scope.shouldShowFullName=function(){`
`return true;`
`}`

-->* css classes for styling error:

### Angularjs css:

* ng-pristine
* ng-dirty
* ng-valid
* ng-invalid

### bootstrap css:

* has-success
* has-warning
* has-error

### username:

`<div class="form-group" ng-class="{'has-error: employee.fullName.$invalid && employeeForm.fullName.$dirty}">`

### email:

`<div class="form-group" ng-class="{'has-error: employee.email.$invalid && employeeForm.email.$dirty}">`

