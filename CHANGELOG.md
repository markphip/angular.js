<a name="1.3.16"></a>
# 1.3.16 cookie-oatmealification (2015-06-05)


## Bug Fixes

- **$compile:** throw error on invalid directive name
  ([634e4671](https://github.com/angular/angular.js/commit/634e467172efa696eb32ef8942ffbedeecbd030e),
   [#11281](https://github.com/angular/angular.js/issues/11281), [#11109](https://github.com/angular/angular.js/issues/11109))
- **$cookies:** update $cookies to prevent duplicate cookie writes and play nice with external code
  ([706a93ab](https://github.com/angular/angular.js/commit/706a93ab6960e3474698ccf9a8048b3c32e567c6),
   [#11490](https://github.com/angular/angular.js/issues/11490), [#11515](https://github.com/angular/angular.js/issues/11515))
- **$http:** throw error if `success` and `error` methods do not receive a function
  ([731e1f65](https://github.com/angular/angular.js/commit/731e1f6534ab7fd1e053b8d7a25c902fcd934fea),
   [#11330](https://github.com/angular/angular.js/issues/11330), [#11333](https://github.com/angular/angular.js/issues/11333))
- **core:** ensure that multiple requests to requestAnimationFrame are buffered
  ([0adc0364](https://github.com/angular/angular.js/commit/0adc0364265b06c567ccc8e90a7f09cc46f235b2),
   [#11791](https://github.com/angular/angular.js/issues/11791))
- **filterFilter:** fix matching against `null`/`undefined`
  ([9dd0fe35](https://github.com/angular/angular.js/commit/9dd0fe35d1027e59b84b2396abee00d8683f3b50),
   [#11573](https://github.com/angular/angular.js/issues/11573), [#11617](https://github.com/angular/angular.js/issues/11617))
- **jqLite:**
  - check for "length" in obj in isArrayLike to prevent iOS8 JIT bug from surfacing
  ([647f3f55](https://github.com/angular/angular.js/commit/647f3f55eb7100a255272f7277f0f962de234a32),
   [#11508](https://github.com/angular/angular.js/issues/11508))
  - attr should ignore comment, text and attribute nodes
  ([181e5ebc](https://github.com/angular/angular.js/commit/181e5ebc3fce5312feacaeace4fcad0d32f4d73c))
- **ngAnimate:**
  - ensure that minified repaint code isn't removed
  ([d5c99ea4](https://github.com/angular/angular.js/commit/d5c99ea42b834343fd0362cfc572f47e7536ccfb),
   [#9936](https://github.com/angular/angular.js/issues/9936))
- **ngAria:** handle elements with role="checkbox/menuitemcheckbox"
  ([1c282af5](https://github.com/angular/angular.js/commit/1c282af5abc205d4aac37c05c5cb725d71747134),
   [#11317](https://github.com/angular/angular.js/issues/11317), [#11321](https://github.com/angular/angular.js/issues/11321))
- **ngModel:** allow setting model to NaN when asyncValidator is present
  ([b64519fe](https://github.com/angular/angular.js/commit/b64519fea7f1a5ec75e32c4b71b012b827314153),
   [#11315](https://github.com/angular/angular.js/issues/11315), [#11411](https://github.com/angular/angular.js/issues/11411))
- **ngTouch:**
  - check undefined tagName for SVG event target
  ([7560a8d2](https://github.com/angular/angular.js/commit/7560a8d2d65955ddb60ede9d586502f4e3cbd062))
  - register touches properly when jQuery is used
  ([40441f6d](https://github.com/angular/angular.js/commit/40441f6dfc5ebd5cdc679c269c4639238f5351eb),
   [#4001](https://github.com/angular/angular.js/issues/4001), [#8584](https://github.com/angular/angular.js/issues/8584), [#10797](https://github.com/angular/angular.js/issues/10797), [#11488](https://github.com/angular/angular.js/issues/11488))
- **select:** prevent unknown option being added to select when bound to null property
  ([9e3f82bb](https://github.com/angular/angular.js/commit/9e3f82bbaf83cad7bb3121db756099b0880562e6),
   [#11872](https://github.com/angular/angular.js/issues/11872), [#11875](https://github.com/angular/angular.js/issues/11875))


## Features

- **travis:** run unit tests on iOS 8
  ([1f650871](https://github.com/angular/angular.js/commit/1f650871266b88b3dab4a894a839a82ac9a06b69),
   [#11479](https://github.com/angular/angular.js/issues/11479))





<a name="1.3.15"></a>
# 1.3.15 locality-filtration (2015-03-17)

## Bug Fixes

- **$animate:** call `applyStyles` with options on `leave`
  ([ebd84e80](https://github.com/angular/angular.js/commit/ebd84e8008f45ccaa84290f6da8c2a114fcfa8cd),
   [#10068](https://github.com/angular/angular.js/issues/10068))
- **$browser:**  don't crash if history.state access causes error in IE
  ([92767c09](https://github.com/angular/angular.js/commit/92767c098feaf8c58faf2d67f882305019d8160e),
   [#10367](https://github.com/angular/angular.js/issues/10367), [#10369](https://github.com/angular/angular.js/issues/10369))
- **Angular:** properly compare RegExp with other objects for equality
  ([b8e8f9af](https://github.com/angular/angular.js/commit/b8e8f9af78f4ef3e556dd3cef6bfee35ad4cb82a),
   [#11204](https://github.com/angular/angular.js/issues/11204), [#11205](https://github.com/angular/angular.js/issues/11205))
- **date filter:** display localised era for `G` format codes
  ([f2683f95](https://github.com/angular/angular.js/commit/f2683f956fcd3216eaa263db20b31e0d46338800),
   [#10503](https://github.com/angular/angular.js/issues/10503), [#11266](https://github.com/angular/angular.js/issues/11266))
- **filterFilter:**
  - fix filtering using an object expression when the filter value is `undefined`
  ([63b9956f](https://github.com/angular/angular.js/commit/63b9956faf4c3679c88a9401b8ccbb111c0294ee),
   [#10419](https://github.com/angular/angular.js/issues/10419), [#10424](https://github.com/angular/angular.js/issues/10424))
  - do not throw an error if property is null when comparing objects
  ([01161a0e](https://github.com/angular/angular.js/commit/01161a0e9fb1af93e9f06535aed8392ed7f116a4),
   [#10991](https://github.com/angular/angular.js/issues/10991), [#10992](https://github.com/angular/angular.js/issues/10992), [#11116](https://github.com/angular/angular.js/issues/11116))
- **form:** allow dynamic form names which initially evaluate to blank
  ([190ea883](https://github.com/angular/angular.js/commit/190ea883c588d63f8b900a8de1d45c6c9ebb01ec),
   [#11096](https://github.com/angular/angular.js/issues/11096))
- **ng/$locale:** add ERA info in generic locale
  ([57842530](https://github.com/angular/angular.js/commit/578425303f2480959da80f31920d08f277d42010))
- **rootScope:** prevent memory leak when destroying scopes
  ([528cf09e](https://github.com/angular/angular.js/commit/528cf09e3f78ad4e3bb6a329ebe315c4f29b4cdb),
   [#11173](https://github.com/angular/angular.js/issues/11173), [#11169](https://github.com/angular/angular.js/issues/11169))
- **templateRequest:** avoid throwing syntax error in Android 2.3
  ([75abbd52](https://github.com/angular/angular.js/commit/75abbd525f07866fdcc6fb311802b8fe700af174),
   [#11089](https://github.com/angular/angular.js/issues/11089), [#11051](https://github.com/angular/angular.js/issues/11051), [#11088](https://github.com/angular/angular.js/issues/11088))


## Features

- **ngAria:**
  - add `button` role to `ngClick`
  ([b9ad91cf](https://github.com/angular/angular.js/commit/b9ad91cf1e86310a2d2bf13b29fa13a9b835e1ce),
   [#9254](https://github.com/angular/angular.js/issues/9254), [#10318](https://github.com/angular/angular.js/issues/10318))
  - add roles to custom inputs
  ([21369943](https://github.com/angular/angular.js/commit/21369943fafd577b36827a641b021b1c14cefb57),
   [#10012](https://github.com/angular/angular.js/issues/10012), [#10318](https://github.com/angular/angular.js/issues/10318))
- **ngMock:**
  - allow mock $controller service to set up controller bindings
  ([b3878a36](https://github.com/angular/angular.js/commit/b3878a36d9f8e56ad7be1eedb9691c9bd12568cb),
   [#9425](https://github.com/angular/angular.js/issues/9425), [#11239](https://github.com/angular/angular.js/issues/11239))
  - add `they` helpers for testing multiple specs
  ([7288be25](https://github.com/angular/angular.js/commit/7288be25a75d6ca6ac7eca05a7d6b12ccb3a22f8),
   [#10864](https://github.com/angular/angular.js/issues/10864))




<a name="1.3.14"></a>
# 1.3.14 instantaneous-browserification (2015-02-24)


## Features

- **CommonJS:** - angular modules are now packaged for npm with helpful exports

## Bug Fixes

- **input:** create max and/or min validator regardless of initial value
  ([abfce532](https://github.com/angular/angular.js/commit/abfce5327ce6fd29c33c62d2edf3600674a6b4c0),
   [#10307](https://github.com/angular/angular.js/issues/10307), [#10327](https://github.com/angular/angular.js/issues/10327))
- **ngAria:** correctly set "checked" attr for checkboxes and radios
  ([944c150e](https://github.com/angular/angular.js/commit/944c150e6c3001e51d4bf5e2d8149ae4c565d1e3),
   [#10389](https://github.com/angular/angular.js/issues/10389), [#10212](https://github.com/angular/angular.js/issues/10212))
- **ngModel:** fix issues when parserName is same as validator key
  ([6b7625a0](https://github.com/angular/angular.js/commit/6b7625a09508c4b5355121a9d4206a734b07b2e1),
   [#10698](https://github.com/angular/angular.js/issues/10698), [#10850](https://github.com/angular/angular.js/issues/10850), [#11046](https://github.com/angular/angular.js/issues/11046))




<a name="1.3.13"></a>
# 1.3.13 meticulous-riffleshuffle (2015-02-09)


## Bug Fixes

- **$location:** prevent page reload if initial url has empty hash at the end
  ([4b3a590b](https://github.com/angular/angular.js/commit/4b3a590b009d7fdceda7f52e7ba0352a271b3256),
   [#10397](https://github.com/angular/angular.js/issues/10397), [#10960](https://github.com/angular/angular.js/issues/10960))
- **ngAria:** ensure native controls fire a single click
  ([69ee593f](https://github.com/angular/angular.js/commit/69ee593fd2cb5f1d7757efbe6b256e4458752fd7),
   [#10388](https://github.com/angular/angular.js/issues/10388), [#10766](https://github.com/angular/angular.js/issues/10766))
- **ngMock:** handle cases where injector is created before tests
  ([39ddef68](https://github.com/angular/angular.js/commit/39ddef682971d3b7282bf9d08f6eaf97b7f4bca4),
   [#10967](https://github.com/angular/angular.js/issues/10967))
- **sanitize:** handle newline characters inside special tags
  ([11aedbd7](https://github.com/angular/angular.js/commit/11aedbd741ccddba060a9805adba1779391731da),
  [ce49d4d6](https://github.com/angular/angular.js/commit/ce49d4d61bd02464b6c6376af8048f6eb09330a8)
   [#10943](https://github.com/angular/angular.js/issues/10943))



<a name="1.3.12"></a>
# 1.3.12 outlandish-knitting (2015-02-02)


## Bug Fixes

- **$controller:** throw better error when controller expression is bad
  ([632b2ddd](https://github.com/angular/angular.js/commit/632b2ddd34c07b3b5a207bd83ca3a5e6e613e63b),
   [#10875](https://github.com/angular/angular.js/issues/10875), [#10910](https://github.com/angular/angular.js/issues/10910))
- **$parse:** remove references to last arguments to a fn call
  ([7caad220](https://github.com/angular/angular.js/commit/7caad2205a6e9927890192a3638f55532bdaaf75),
   [#10894](https://github.com/angular/angular.js/issues/10894))
- **ngRoute:** dont duplicate optional params into query
  ([f41ca4a5](https://github.com/angular/angular.js/commit/f41ca4a53ed53f172fb334911be56e42aad58794),
   [#10689](https://github.com/angular/angular.js/issues/10689))
- **ngScenario:** Allow ngScenario to handle lazy-loaded and manually bootstrapped applications
  ([0bcd0872](https://github.com/angular/angular.js/commit/0bcd0872d8d2e37e6cb7aa5bc5cb0c742b4294f9),
   [#10723](https://github.com/angular/angular.js/issues/10723))
- **validators:** maxlength should use viewValue for $isEmpty
  ([abd8e2a9](https://github.com/angular/angular.js/commit/abd8e2a9eb2d21ac67989c2f7b64c4c6547a1585),
   [#10898](https://github.com/angular/angular.js/issues/10898))


## Features

- **ngMocks:** cleanup $inject annotations after each test
  ([6ec59460](https://github.com/angular/angular.js/commit/6ec5946094ee92b820bbacc886fa2367715e60b4))



<a name="1.3.11"></a>
# 1.3.11 spiffy-manatee (2015-01-26)


## Bug Fixes

- **$location:** don't rewrite when link is shift-clicked
  ([939ca37c](https://github.com/angular/angular.js/commit/939ca37cfe5f6fc35b09b6705caabd1fcc3cf9d3),
   [#9904](https://github.com/angular/angular.js/issues/9904), [#9906](https://github.com/angular/angular.js/issues/9906))
- **htmlAnchorDirective:**
  - remove "element !== target element" check
  ([779e3f6b](https://github.com/angular/angular.js/commit/779e3f6b5f8d2550e758cb0c5f64187ba8e00e29),
   [#10866](https://github.com/angular/angular.js/issues/10866))
  - don't add event listener if replaced, ignore event if target is different element
  ([837a0775](https://github.com/angular/angular.js/commit/837a077578081bbd07863bef85241537d19fa652),
   [#4262](https://github.com/angular/angular.js/issues/4262), [#10849](https://github.com/angular/angular.js/issues/10849))



<a name="1.3.10"></a>
# 1.3.10 heliotropic-sundial (2015-01-20)


## Bug Fixes

- **$animate:** ensure no transitions are applied when an empty inline style object is provided
  ([9b8df52a](https://github.com/angular/angular.js/commit/9b8df52aa960b9b6288fc150d55ea2e35f56555e),
   [#10613](https://github.com/angular/angular.js/issues/10613), [#10770](https://github.com/angular/angular.js/issues/10770))
- **$compile:** support class directives on SVG elements
  ([7a9e3360](https://github.com/angular/angular.js/commit/7a9e3360284d58197a1fe34de57f5e0f6d1f4a76),
   [#10736](https://github.com/angular/angular.js/issues/10736), [#10756](https://github.com/angular/angular.js/issues/10756))
- **form:** clean up success state of controls when they are removed
  ([cdc7280d](https://github.com/angular/angular.js/commit/cdc7280dd3d5a2ded784c06dd55fe36c2053fb6f),
   [#10509](https://github.com/angular/angular.js/issues/10509))
- **ngController:** allow bound constructor fns as controllers
  ([d015c8a8](https://github.com/angular/angular.js/commit/d015c8a80b28754633c846fc50d11c9437519486),
   [#10784](https://github.com/angular/angular.js/issues/10784), [#10790](https://github.com/angular/angular.js/issues/10790))



<a name="1.3.9"></a>
# 1.3.9 multidimensional-awareness (2015-01-13)


## Bug Fixes

- **$parse:** allow use of locals in assignments
  ([86900814](https://github.com/angular/angular.js/commit/869008140a96e0e9e0d9774cc2e5fdd66ada7ba9))
- **filterFilter:** use isArray() to determine array type
  ([d4b60ada](https://github.com/angular/angular.js/commit/d4b60ada1ecff5afdb3210caa44e149e9f3d4c1b),
   [#10621](https://github.com/angular/angular.js/issues/10621))


## Features

- **ngMock/$exceptionHandler:** log errors when rethrowing
  ([2b97854b](https://github.com/angular/angular.js/commit/2b97854bf4786fe8579974e2b9d6b4adee8a3dc3),
   [#10540](https://github.com/angular/angular.js/issues/10540), [#10564](https://github.com/angular/angular.js/issues/10564))


## Performance Improvements

- **ngStyleDirective:** use $watchCollection
  ([4c8d8ad5](https://github.com/angular/angular.js/commit/4c8d8ad5083d9dd17c0b8480339d5f95943f1b71),
   [#10535](https://github.com/angular/angular.js/issues/10535))




<a name="1.3.8"></a>
# 1.3.8 prophetic-narwhal (2014-12-19)


## Bug Fixes
- **filterFilter:**
  - make `$` match properties on deeper levels as well
  ([bd28c74c](https://github.com/angular/angular.js/commit/bd28c74c1d91c477a86f10fe36576cba0249e6ef),
   [#10401](https://github.com/angular/angular.js/issues/10401))
  - let expression object `{$: '...'}` also match primitive items
  ([fb2c5858](https://github.com/angular/angular.js/commit/fb2c58589758744c0eef8c2ead3dbcf27a5cf200),
   [#10428](https://github.com/angular/angular.js/issues/10428))
- **ngAria:** trigger digest on `ng-click` via keypress, pass `$event` to expression
  ([924e68c7](https://github.com/angular/angular.js/commit/924e68c7d522a1086969f3583d0ce87e59110bc5),
   [#10442](https://github.com/angular/angular.js/issues/10442), [#10443](https://github.com/angular/angular.js/issues/10443), [#10447](https://github.com/angular/angular.js/issues/10447))
- **orderBy:** compare timestamps when sorting date objects
  ([661f6d9e](https://github.com/angular/angular.js/commit/661f6d9ecf1459ce3b2794c3cde373e17ae83972),
   [#10512](https://github.com/angular/angular.js/issues/10512), [#10516](https://github.com/angular/angular.js/issues/10516))


## Performance Improvements

- **limitTo:** replace for loop with slice
  ([cd77c089](https://github.com/angular/angular.js/commit/cd77c089ba2f4b94ccc74f32f0ffa9fb70851c02))




<a name="1.3.7"></a>
# 1.3.7 leaky-obstruction (2014-12-15)


## Bug Fixes

- **$compile:** use `createMap()` for `$$observe` listeners when initialized from attr interpolation
  ([8e28bb4c](https://github.com/angular/angular.js/commit/8e28bb4c2f6d015dfe1cec7755f1ca9b0ecef1f8))
- **$http:**
  - only parse as JSON when opening/closing brackets match
  ([b9bdbe61](https://github.com/angular/angular.js/commit/b9bdbe615cc4070d2233ff06830a4c6fb1217cda),
   [#10349](https://github.com/angular/angular.js/issues/10349), [#10357](https://github.com/angular/angular.js/issues/10357))
  - don't convert FormData objects to JSON
  ([40258838](https://github.com/angular/angular.js/commit/40258838031604feecb862afdc6f1f503d80ce4a),
   [#10373](https://github.com/angular/angular.js/issues/10373))
- **$parse:** a chain of field accessors should use a single `getterFn`
  ([c90ad968](https://github.com/angular/angular.js/commit/c90ad96808be350526516626205c3a7d1da79024))
- **ngRepeat:** allow extra whitespaces in `(key,value)` part of micro-syntax
  ([ef640cbc](https://github.com/angular/angular.js/commit/ef640cbc2af5794c987e75472c12e63a59590044),
   [#6827](https://github.com/angular/angular.js/issues/6827), [#6833](https://github.com/angular/angular.js/issues/6833))
- **orderBy:** do not try to call `valueOf`/`toString` on `null`
  ([a097aa95](https://github.com/angular/angular.js/commit/a097aa95b7c78beab6d1b7d521c25f7d9d7843d9),
   [#10385](https://github.com/angular/angular.js/issues/10385), [#10386](https://github.com/angular/angular.js/issues/10386))


## Features

- **$compile:** add support for `ng-attr` with camelCased attributes
  ([d8e37078](https://github.com/angular/angular.js/commit/d8e37078600089839f82f0e84022f1087e1fd3f2),
   [#9845](https://github.com/angular/angular.js/issues/9845), [#10194](https://github.com/angular/angular.js/issues/10194))
- **$http:** pass response status code to data transform functions
  ([1b740974](https://github.com/angular/angular.js/commit/1b740974f5eb373bed04071d51f908ced7c5a8e5),
   [#10324](https://github.com/angular/angular.js/issues/10324), [#6734](https://github.com/angular/angular.js/issues/6734), [#10440](https://github.com/angular/angular.js/issues/10440))
- **$rootScope:** allow passing `locals` argument to `$evalAsync`
  ([9b96cea4](https://github.com/angular/angular.js/commit/9b96cea462676d123e1b2dd852aedbe3da8fa4a0),
   [#10390](https://github.com/angular/angular.js/issues/10390))


## Performance Improvements

- **$compile:** only re-`$interpolate` attribute values at link time if changed since compile
  ([9ae0c01c](https://github.com/angular/angular.js/commit/9ae0c01c2bcaff2f3906eec574f9c6ed8abde14a))


## Breaking Changes

- **orderBy:** due to [a097aa95](https://github.com/angular/angular.js/commit/a097aa95b7c78beab6d1b7d521c25f7d9d7843d9),

Previously, if either value being compared in the orderBy comparator was null or undefined, the
order would, incorrectly, not change. Now, this order behaves more like Array.prototype.sort, which
by default pushes `null` behind objects, due to `n` occurring after `[` (the first characters of their
stringified forms) in ASCII / Unicode. If `toString` is customized, or does not exist, the
behaviour is undefined.



<a name="1.3.6"></a>
# 1.3.6 robofunky-danceblaster (2014-12-08)


## Bug Fixes

- **$browser:** prevent infinite digests when clearing the hash of a url
  ([10ac5948](https://github.com/angular/angular.js/commit/10ac5948097e2c8eaead238603d29ee580dc8273),
   [#9629](https://github.com/angular/angular.js/issues/9629), [#9635](https://github.com/angular/angular.js/issues/9635), [#10228](https://github.com/angular/angular.js/issues/10228), [#10308](https://github.com/angular/angular.js/issues/10308))
- **$http:** preserve config object when resolving from cache
  ([facfec98](https://github.com/angular/angular.js/commit/facfec98412c0bb8678d578bade05ffef06a9e84),
   [#9004](https://github.com/angular/angular.js/issues/9004), [#9030](https://github.com/angular/angular.js/issues/9030))
- **$location:**
  - allow hash fragments with hashPrefix in hash-bang location urls
  ([2dc34a96](https://github.com/angular/angular.js/commit/2dc34a969956eea680be4c8d9f800556d110996a),
   [#9629](https://github.com/angular/angular.js/issues/9629), [#9635](https://github.com/angular/angular.js/issues/9635), [#10228](https://github.com/angular/angular.js/issues/10228), [#10308](https://github.com/angular/angular.js/issues/10308))
  - strip off empty hash segments when comparing
  ([e93710fe](https://github.com/angular/angular.js/commit/e93710fe0e4fb05ceee59a04f290692a5bec5d20),
   [#9635](https://github.com/angular/angular.js/issues/9635))
- **$parse:**
  - fix operators associativity
  ([ed1243ff](https://github.com/angular/angular.js/commit/ed1243ffc7c2cb4bd5b4dece597597db8eb08e34))
  - follow JavaScript context for unbound functions
  ([429938da](https://github.com/angular/angular.js/commit/429938da1f45b8a649b8c77762fb0ae59b6d0cea))
- **filterFilter:**
  - don't match primitive sub-expressions against any prop
  ([a75537d4](https://github.com/angular/angular.js/commit/a75537d461c92e3455e372ff5005bf0cad2d2e95))
  - ignore function properties and account for inherited properties
  ([5ced914c](https://github.com/angular/angular.js/commit/5ced914cc8625008e6249d5ac5942d5822287cc0),
   [#9984](https://github.com/angular/angular.js/issues/9984))
  - correctly handle deep expression objects
  ([f7cf8460](https://github.com/angular/angular.js/commit/f7cf846045b1e2fb39c62e304c61b44d5c805e31),
   [#7323](https://github.com/angular/angular.js/issues/7323), [#9698](https://github.com/angular/angular.js/issues/9698), [#9757](https://github.com/angular/angular.js/issues/9757))
- **inputs:** ignoring input events in IE caused by placeholder changes or focus/blur on inputs with placeholders
  ([55d9db56](https://github.com/angular/angular.js/commit/55d9db56a6f7d29b16f8393612648080c6d535d6),
   [#9265](https://github.com/angular/angular.js/issues/9265))
- **linky:** make urls starting with www. links, like markdown
  ([915a891a](https://github.com/angular/angular.js/commit/915a891ad4cdcaa5e47e976db8f4d402d230be77),
   [#10290](https://github.com/angular/angular.js/issues/10290))
- **ngAnimate:** do not use jQuery class API
  ([40a537c2](https://github.com/angular/angular.js/commit/40a537c25f70ad556a41bb2d00ea3e257410e9af),
   [#10024](https://github.com/angular/angular.js/issues/10024), [#10329](https://github.com/angular/angular.js/issues/10329))
- **ngMock:** allow numeric timeouts in $httpBackend mock
  ([acb066e8](https://github.com/angular/angular.js/commit/acb066e84a10483e1025eed295352b66747dbb8a),
   [#4891](https://github.com/angular/angular.js/issues/4891))
- **ngModel:**
  - always use the most recent viewValue for validation
  ([2d6a0a1d](https://github.com/angular/angular.js/commit/2d6a0a1dc1e7125cab2e30244e35e97e11802843),
   [#10126](https://github.com/angular/angular.js/issues/10126), [#10299](https://github.com/angular/angular.js/issues/10299))
  - fixing many keys incorrectly marking inputs as dirty
  ([d21dff21](https://github.com/angular/angular.js/commit/d21dff21ed8beb015ad911f11d57cceb56fc439f))
- **ngSanitize:** exclude smart quotes at the end of the link
  ([7c6be43e](https://github.com/angular/angular.js/commit/7c6be43e83590798cffef63d076fb79d5296fba2),
   [#7307](https://github.com/angular/angular.js/issues/7307))
- **numberFilter:** numbers rounding to zero shouldn't be negative
  ([96c61fe7](https://github.com/angular/angular.js/commit/96c61fe756d7d3db011818bf0925e3d86ffff8ce),
   [#10278](https://github.com/angular/angular.js/issues/10278))
- **orderBy:**
  - make object-to-primtiive behaviour work for objects with null prototype
  ([3aa57528](https://github.com/angular/angular.js/commit/3aa5752894419b4638d5c934879258fa6a1c0d07))
  - maintain order in array of objects when predicate is not provided
  ([8bfeddb5](https://github.com/angular/angular.js/commit/8bfeddb5d671017f4a21b8b46334ac816710b143),
   [#9566](https://github.com/angular/angular.js/issues/9566), [#9747](https://github.com/angular/angular.js/issues/9747), [#10311](https://github.com/angular/angular.js/issues/10311))


## Features

- **$$jqLite:** export jqLite as a private service
  ([f2e7f875](https://github.com/angular/angular.js/commit/f2e7f875e2ad4b271c4e72ebd3860f905132eed9))
- **$injector:** print caller name in "unknown provider" errors (when available)
  ([013b522c](https://github.com/angular/angular.js/commit/013b522c9e690665aecb0e0f656e4557a673ec09),
   [#8135](https://github.com/angular/angular.js/issues/8135), [#9721](https://github.com/angular/angular.js/issues/9721))
- **jsonFilter:** add optional arg to define custom indentation
  ([1191edba](https://github.com/angular/angular.js/commit/1191edba4eaa15f675fa4ed047949a150843971b),
   [#9771](https://github.com/angular/angular.js/issues/9771))
- **ngAria:** bind keypress on ng-click w/ option
  ([5481e2cf](https://github.com/angular/angular.js/commit/5481e2cfcd4d136a1c7f45cd4ce0fa1a8a15074d),
   [#10288](https://github.com/angular/angular.js/issues/10288))


## Breaking Changes

- **$location:** due to [2dc34a96](https://github.com/angular/angular.js/commit/2dc34a969956eea680be4c8d9f800556d110996a),


We no longer throw an `ihshprfx` error if the URL after the base path
contains only a hash fragment.  Previously, if the base URL was `http://abc.com/base/`
and the hashPrefix is `!` then trying to parse `http://abc.com/base/#some-fragment`
would have thrown an error. Now we simply assume it is a normal fragment and
that the path is empty, resulting `$location.absUrl() === "http://abc.com/base/#!/#some-fragment"`.

This should not break any applications, but you can no longer rely on receiving the
`ihshprfx` error for paths that have the syntax above. It is actually more similar
to what currently happens for invalid extra paths anyway:  If the base URL
and hashPrfix are set up as above, then `http://abc.com/base/other/path` does not
throw an error but just ignores the extra path: `http://abc.com/base`.


- **filterFilter:** due to [a75537d4](https://github.com/angular/angular.js/commit/a75537d461c92e3455e372ff5005bf0cad2d2e95),

  Named properties in the expression object will only match against properties on the **same level**.
  Previously, named string properties would match against properties on the same level **or deeper**.

    Before:

    ```js
    arr = filterFilter([{level1: {level2: 'test'}}], {level1: 'test'});   // arr.length -> 1
    ```

    After:

    ```js
    arr = filterFilter([{level1: {level2: 'test'}}], {level1: 'test'});   // arr.length -> 0
    ```

    In order to match deeper nested properties, you have to either match the depth level of the
    property or use the special `$` key (which still matches properties on the same level
    **or deeper**). E.g.:

    ```js
    // Both examples below have `arr.length === 1`
    arr = filterFilter([{level1: {level2: 'test'}}], {level1: {level2: 'test'}});
    arr = filterFilter([{level1: {level2: 'test'}}], {$: 'test'});
    ```


<a name="1.3.5"></a>
# 1.3.5 cybernetic-mercantilism (2014-12-01)


## Bug Fixes

- **$templateRequest:** propagate rejection reason when ignoreRequestError flag is set
  ([f6458826](https://github.com/angular/angular.js/commit/f6458826ac974914597a10b0ffdeee3c5d2c62ef),
   [#10266](https://github.com/angular/angular.js/issues/10266))
- **$httpBackend:** allow canceling request with falsy timeoutId
  ([719d5c5f](https://github.com/angular/angular.js/commit/719d5c5fa59ae1617691a0dca02da861fcf5f933),
   [#10177](https://github.com/angular/angular.js/issues/10177))
- **linky:** encode all double quotes when serializing email addresses
  ([2ec8d1ff](https://github.com/angular/angular.js/commit/2ec8d1ffc04e06a39cb1b74a8d675da38e0a1c6b),
   [#10090](https://github.com/angular/angular.js/issues/10090))
- **ngMock:**
  - annotate $RootScopeDecorator
  ([9a83f9d2](https://github.com/angular/angular.js/commit/9a83f9d2fabe0a259c283b7f7cd935e4b36e2b5d),
   [#10273](https://github.com/angular/angular.js/issues/10273), [#10275](https://github.com/angular/angular.js/issues/10275), [#10277](https://github.com/angular/angular.js/issues/10277))
  - respond did not always take a statusText argument
  ([08cd5c19](https://github.com/angular/angular.js/commit/08cd5c19c7a5116e7e74691391fc5e28bfae4521),
   [#8270](https://github.com/angular/angular.js/issues/8270))
- **select:**
  - use strict compare when removing option from ctrl
  ([9fa73cb4](https://github.com/angular/angular.js/commit/9fa73cb4e7190b4d00b65f2f8f9f7d37607308ba),
   [#9714](https://github.com/angular/angular.js/issues/9714), [#10115](https://github.com/angular/angular.js/issues/10115), [#10203](https://github.com/angular/angular.js/issues/10203))
  - fix several issues when moving options between groups
  ([30694c80](https://github.com/angular/angular.js/commit/30694c802763d46d6787f7298f47dfef53ed4229),
   [#10166](https://github.com/angular/angular.js/issues/10166))


<a name="1.3.4"></a>
# 1.3.4 highfalutin-petroglyph (2014-11-24)

## Bug Fixes

- **$browser:** allow chaining url() calls in setter mode
  ([764fa869](https://github.com/angular/angular.js/commit/764fa869dd8809d494924c23f30ddaa4cac84249),
   [#10157](https://github.com/angular/angular.js/issues/10157))
- **$http:** return empty headers, ignore properties in Object prototype
  ([637c020f](https://github.com/angular/angular.js/commit/637c020f828a7ceeaacf83bb1a54ed3092e6c273),
   [#7779](https://github.com/angular/angular.js/issues/7779), [#10113](https://github.com/angular/angular.js/issues/10113), [#10091](https://github.com/angular/angular.js/issues/10091))
- **$locale:** Allow currency filter to fall back to maxFrac from locale
  ([6dbd606a](https://github.com/angular/angular.js/commit/6dbd606ad7b708d5886c0e7ffee20ae8f8719711),
   [#10179](https://github.com/angular/angular.js/issues/10179))
- **$location:** allow empty string URLs to reset path, search, and hash
  ([7812dfce](https://github.com/angular/angular.js/commit/7812dfcee8ab98cbf38261f9948d9541656bf554),
   [#10063](https://github.com/angular/angular.js/issues/10063), [#10064](https://github.com/angular/angular.js/issues/10064))
- **$route:** fix redirection with optional/eager params
  ([891acf4c](https://github.com/angular/angular.js/commit/891acf4c201823fd2c925ee321c70d06737d5944),
   [#9819](https://github.com/angular/angular.js/issues/9819), [#9827](https://github.com/angular/angular.js/issues/9827))
- **Angular:** properly get node name for svg element wrapper
  ([09a98323](https://github.com/angular/angular.js/commit/09a9832358960c98392c9df1a9fd9592f59bc844),
   [#10078](https://github.com/angular/angular.js/issues/10078), [#10172](https://github.com/angular/angular.js/issues/10172))
- **NgModelController:** typo $rawModelValue -> $$rawModelValue
  ([4f4ff5f3](https://github.com/angular/angular.js/commit/4f4ff5f31b82c6f7be409ea4edbad4c2913ac1f1))
- **input:**
  - set ngTrueValue on required checkbox
  ([8692f87a](https://github.com/angular/angular.js/commit/8692f87a4689fa0dd3640f4dcab5c6b6f960489b),
   [#5164](https://github.com/angular/angular.js/issues/5164))
  - call $setTouched in blur asynchronously if necessary
  ([eab27187](https://github.com/angular/angular.js/commit/eab271876cb87c1f5f6c6f29e814fb8fecad87ff),
   [#8762](https://github.com/angular/angular.js/issues/8762), [#9808](https://github.com/angular/angular.js/issues/9808), [#10014](https://github.com/angular/angular.js/issues/10014))
- **input[date]:** do not use `$isEmpty` to check the model validity
  ([40406e2f](https://github.com/angular/angular.js/commit/40406e2f22713efbd37ef3eff408339727cb62d9))
- **linky:** encode double quotes when serializing email addresses
  ([8ee8ffeb](https://github.com/angular/angular.js/commit/8ee8ffeba0a5a133fa792745c1019d294ecfcef3),
   [#8945](https://github.com/angular/angular.js/issues/8945), [#8964](https://github.com/angular/angular.js/issues/8964), [#5946](https://github.com/angular/angular.js/issues/5946), [#10090](https://github.com/angular/angular.js/issues/10090), [#9256](https://github.com/angular/angular.js/issues/9256))
- **ngMaxlength:** ignore maxlength when not set to a non-negative integer
  ([92f87b11](https://github.com/angular/angular.js/commit/92f87b114242b01876e1dc5c6fddd061352ecb2c),
   [#9874](https://github.com/angular/angular.js/issues/9874))
- **ngModel:** don't run parsers when executing $validate
  ([e3764e30](https://github.com/angular/angular.js/commit/e3764e30a301ec6136c8e6b5493d39feb3cd1ecc))
- **ngModelOptions:** preserve context of getter/setters
  ([bb4d3b73](https://github.com/angular/angular.js/commit/bb4d3b73a1ccf3dee55b0c25baf031bae5cbb676),
   [#9394](https://github.com/angular/angular.js/issues/9394), [#9865](https://github.com/angular/angular.js/issues/9865))


## Features

- **ngMaxlength:** add support for disabling max length limit
  ([5c1fdff6](https://github.com/angular/angular.js/commit/5c1fdff691b9367d73f72f6a0298cb6a6e259f35),
   [#9995](https://github.com/angular/angular.js/issues/9995))
- **ngModelController:** add $setDirty method
  ([e8941c0f](https://github.com/angular/angular.js/commit/e8941c0fe5217d2e705bad8253dc0162aff4c709),
   [#10038](https://github.com/angular/angular.js/issues/10038), [#10049](https://github.com/angular/angular.js/issues/10049))
- **ngPluralize:** add support for `count` to be a one-time expression
  ([2b41a586](https://github.com/angular/angular.js/commit/2b41a5868aee79e3872ad92db66e30959207d98e),
   [#10004](https://github.com/angular/angular.js/issues/10004))


## Performance Improvements

- use Object.create instead of creating temporary constructors
  ([bf6a79c3](https://github.com/angular/angular.js/commit/bf6a79c3484f474c300b5442ae73483030ef5782),
   [#10058](https://github.com/angular/angular.js/issues/10058))


## Breaking Changes

- **ngModelOptions:** due to [bb4d3b73](https://github.com/angular/angular.js/commit/bb4d3b73a1ccf3dee55b0c25baf031bae5cbb676),
  previously, ngModel invoked getter/setters in the global context.

For example:

```js
<input ng-model="model.value" ng-model-options="{ getterSetter: true }">
```

would previously invoke `model.value()` in the global context.

Now, ngModel invokes `value` with `model` as the context.

It's unlikely that real apps relied on this behavior. If they did they can use `.bind` to explicilty
bind a getter/getter to the global context, or just reference globals normally without `this`.



<a name="1.3.3"></a>
# 1.3.3 undersea-arithmetic (2014-11-17)


## Bug Fixes

- **$http:** don't parse single space responses as JSON
  ([6f19a6fd](https://github.com/angular/angular.js/commit/6f19a6fd33ab72d3908e3418fba47ee8e1598fa6),
   [#9907](https://github.com/angular/angular.js/issues/9907))
- **minErr:** stringify non-JSON compatible objects in error messages
  ([cf43ccdf](https://github.com/angular/angular.js/commit/cf43ccdf9b8665a2fd5d6aa52f80cb2d7c9bb7e2),
   [#10085](https://github.com/angular/angular.js/issues/10085))
- **$rootScope:** handle cyclic references in scopes when creating error messages
  ([e80053d9](https://github.com/angular/angular.js/commit/e80053d91fd7c722e092a23d326384de2e552eb6),
   [#10085](https://github.com/angular/angular.js/issues/10085))
- **ngRepeat:** support cyclic object references in error messages
  ([fa12c3c8](https://github.com/angular/angular.js/commit/fa12c3c86af7965d1b9d9a5dd3434755e9e04635),
   [#9838](https://github.com/angular/angular.js/issues/9838), [#10065](https://github.com/angular/angular.js/issues/10065), [#10085](https://github.com/angular/angular.js/issues/10085))
- **ngMock:** call $interval callbacks even when invokeApply is false
  ([d81ff888](https://github.com/angular/angular.js/commit/d81ff8885b77f70c6417d7be3124d86d07447375),
   [#10032](https://github.com/angular/angular.js/issues/10032))
- **ngPattern:** match behaviour of native HTML pattern attribute
  ([85eb9660](https://github.com/angular/angular.js/commit/85eb9660ef67c24d5104a6a1921bedad0bd1b57e),
   [#9881](https://github.com/angular/angular.js/issues/9881), [#9888](https://github.com/angular/angular.js/issues/9888))
- **select:** ensure the label attribute is updated in Internet Explorer
  ([6604c236](https://github.com/angular/angular.js/commit/6604c2361427fba8c43a39dc2e92197390dfbdbe),
   [#9621](https://github.com/angular/angular.js/issues/9621), [#10042](https://github.com/angular/angular.js/issues/10042))


## Features

- **$location:** allow to location to be changed during $locationChangeStart
  ([a9352c19](https://github.com/angular/angular.js/commit/a9352c19ce33f0393d6581547c7ea8dfc2a8b78f),
   [#9607](https://github.com/angular/angular.js/issues/9607), [#9678](https://github.com/angular/angular.js/issues/9678))
- **$routeProvider:** allow setting caseInsensitiveMatch on the provider
  ([0db573b7](https://github.com/angular/angular.js/commit/0db573b7493f76abd94ff65ce660017d617e865b),
   [#6477](https://github.com/angular/angular.js/issues/6477), [#9873](https://github.com/angular/angular.js/issues/9873))


## Performance Improvements

- **orderBy:** copy array with slice instead of for loop
  ([8eabc546](https://github.com/angular/angular.js/commit/8eabc5463c795d87f37e5a9eacbbb14435024061),
   [#9942](https://github.com/angular/angular.js/issues/9942))

## Breaking Changes

- **$parse:** due to [fbad2805](https://github.com/angular/angular.js/commit/fbad2805703569058a4a860747b0e2d8aee36bdf),
    you can't use characters that have special meaning in AngularJS expressions (ex.: `.` or `-`)
    as part of filter's name. Before this commit custom filters could contain special characters
    (like a dot) in their name but this wasn't intentional.

<a name="1.3.2"></a>
# 1.3.2 cardiovasculatory-magnification (2014-11-07)


## Bug Fixes

- **$compile:** do not rebind parent bound transclude functions
  ([841c0907](https://github.com/angular/angular.js/commit/841c0907556f525dbc4223609d808319fe0dd7e2),
   [#9413](https://github.com/angular/angular.js/issues/9413))
- **$parse:**
  - stateful interceptors override an `undefined` expression
  ([ed99821e](https://github.com/angular/angular.js/commit/ed99821e4dc621864f7e2d9a6b5305fca27fb7fa),
   [#9821](https://github.com/angular/angular.js/issues/9821), [#9825](https://github.com/angular/angular.js/issues/9825))
  - add quick check for Function constructor in fast path
  ([e676d642](https://github.com/angular/angular.js/commit/e676d642f5feb8d3ba88944634afb479ba525c36))
- **$parse, events:** prevent accidental misuse of properties on $event
  ([e057a9aa](https://github.com/angular/angular.js/commit/e057a9aa398ead209bd6bbf76e22d2d5562904fb))
- **ngRoute:** allow proto inherited properties in route params object
  ([b4770582](https://github.com/angular/angular.js/commit/b4770582f84f26c8ff7f2320a36a6b0ceff6e6cc),
   [#8181](https://github.com/angular/angular.js/issues/8181), [#9731](https://github.com/angular/angular.js/issues/9731))
- **select:** use strict comparison for isSelected with selectAs
  ([9e305948](https://github.com/angular/angular.js/commit/9e305948e4965fb86b0c79985dc6e8c59a9c66af),
   [#9639](https://github.com/angular/angular.js/issues/9639), [#9949](https://github.com/angular/angular.js/issues/9949))


## Features

- **ngAria:** announce ngMessages with aria-live
  ([187e4318](https://github.com/angular/angular.js/commit/187e43185dfb1bce6a318d95958c73cfb789d33c),
   [#9834](https://github.com/angular/angular.js/issues/9834))
- **ngMock:** decorator that adds Scope#$countChildScopes and Scope#$countWatchers
  ([74981c9f](https://github.com/angular/angular.js/commit/74981c9f208b3617cbf00beafd61138d25c5d546),
   [#9926](https://github.com/angular/angular.js/issues/9926), [#9871](https://github.com/angular/angular.js/issues/9871))


##  Security Note

This release also contains security fixes for expression sandbox bypasses.

These issues affect only applications with known server-side XSS holes that are also using [CSP](https://developer.mozilla.org/en-US/docs/Web/Security/CSP) to secure their client-side code. If your application falls into this rare category, we recommend updating your version of Angular.

We'd like to thank security researches [Sebastian Lekies](https://twitter.com/sebastianlekies), [Jann Horn](http://thejh.net/), and [Gábor Molnár](https://twitter.com/molnar_g) for reporting these issues to us.

We also added a documentation page focused on security, which contains some of the best practices, DOs and DON'Ts. Please check out [https://docs.angularjs.org/guide/security](https://docs.angularjs.org/guide/security).



<a name="1.3.1"></a>
# 1.3.1 spectral-lobster (2014-10-31)


## Bug Fixes

- **$compile:** returning null when an optional controller is not found
  ([2cd5b4ec](https://github.com/angular/angular.js/commit/2cd5b4ec4409a818ccd33a6fbdeb99a3443a1809),
   [#9404](https://github.com/angular/angular.js/issues/9404), [#9392](https://github.com/angular/angular.js/issues/9392))
- **$observe:** check if the attribute is undefined
  ([531a8de7](https://github.com/angular/angular.js/commit/531a8de72c439d8ddd064874bf364c00cedabb11),
   [#9707](https://github.com/angular/angular.js/issues/9707), [#9720](https://github.com/angular/angular.js/issues/9720))
- **$parse:** support dirty-checking objects with null prototype
  ([28661d1a](https://github.com/angular/angular.js/commit/28661d1a8cc3a8454bad7ae531e027b1256476c9),
   [#9568](https://github.com/angular/angular.js/issues/9568))
- **$sce:** use msie instead of $document[0].documentMode
  ([45252c3a](https://github.com/angular/angular.js/commit/45252c3a545336a0bac93be6ee28cde6afaa3cb4),
   [#9661](https://github.com/angular/angular.js/issues/9661))
- **$templateRequest:** ignore JSON Content-Type header and content
  ([1bd473eb](https://github.com/angular/angular.js/commit/1bd473eb4587900086e0b6b308dcf1dcfe9760d9),
   [#5756](https://github.com/angular/angular.js/issues/5756), [#9619](https://github.com/angular/angular.js/issues/9619))
- **i18n:** rename datetimeSymbols to be camelCase
  ([94f5a285](https://github.com/angular/angular.js/commit/94f5a285bfcf04d800afc462a7a37a3469d77f1a))
- **loader:** fix double spaces
  ([8b2f1a47](https://github.com/angular/angular.js/commit/8b2f1a47b584ceb98689f48538a2af73cd65dfd8),
   [#9630](https://github.com/angular/angular.js/issues/9630))
- **ngMock:** $httpBackend should match data containing Date objects correctly
  ([1025f6eb](https://github.com/angular/angular.js/commit/1025f6ebf4e5933a12920889be00cd8ac8a106fa),
   [#5127](https://github.com/angular/angular.js/issues/5127))
- **ngSanitize:** attribute name: xmlns:href -> xlink:href
  ([4cccf0f2](https://github.com/angular/angular.js/commit/4cccf0f2a89b002d63cb443e1e7b15f76dcef425),
   [#9769](https://github.com/angular/angular.js/issues/9769))
- **select:** assign result of track exp to element value
  ([4b4098bf](https://github.com/angular/angular.js/commit/4b4098bfcae64f69c70a22393de1f3d9a0d3dc46),
   [#9718](https://github.com/angular/angular.js/issues/9718), [#9592](https://github.com/angular/angular.js/issues/9592))
- **templateRequest:** allow empty html template
  ([52ceec22](https://github.com/angular/angular.js/commit/52ceec2229dc132b76da4e022c91474344f2d906),
   [#9581](https://github.com/angular/angular.js/issues/9581))
- **testability:** escape regex chars in `findBindings` if using `exactMatch`
  ([02aa4f4b](https://github.com/angular/angular.js/commit/02aa4f4b85ee15922a1f2de8ba78f562c18518d0),
   [#9595](https://github.com/angular/angular.js/issues/9595), [#9600](https://github.com/angular/angular.js/issues/9600))


## Features

- **$compile:** allow $watchCollection to be used in bi-directional bindings
  ([40bbc981](https://github.com/angular/angular.js/commit/40bbc9817845bf75581daee5d0ec30980affb0f5),
   [#9725](https://github.com/angular/angular.js/issues/9725))
- **ngSanitize:** accept SVG elements and attributes
  ([a54b25d7](https://github.com/angular/angular.js/commit/a54b25d77999a85701dfc5396fef78e586a99667),
   [#9578](https://github.com/angular/angular.js/issues/9578), [#9751](https://github.com/angular/angular.js/issues/9751))




<a name="1.3.0"></a>
# 1.3.0 superluminal-nudge (2014-10-13)


## Bug Fixes

- **$browser:**
  - account for IE deserializing history.state on each read
  ([1efaf3dc](https://github.com/angular/angular.js/commit/1efaf3dc136f822703a9cda55afac7895a923ccb),
   [#9587](https://github.com/angular/angular.js/issues/9587), [#9545](https://github.com/angular/angular.js/issues/9545))
  - do not decode cookies that do not appear encoded
  ([9c995905](https://github.com/angular/angular.js/commit/9c9959059eb84f0f1d748b70b50ec47b7d23d065),
   [#9211](https://github.com/angular/angular.js/issues/9211), [#9225](https://github.com/angular/angular.js/issues/9225))
- **$http:**
  - allow empty json response
  ([9ba24c54](https://github.com/angular/angular.js/commit/9ba24c54d60e643b1450cc5cfa8f990bd524c130),
   [#9532](https://github.com/angular/angular.js/issues/9532), [#9562](https://github.com/angular/angular.js/issues/9562))
  - don't run transformData on HEAD methods
  ([6e4955a3](https://github.com/angular/angular.js/commit/6e4955a3086555d8ca30c29955faa213b39c6f27),
   [#9528](https://github.com/angular/angular.js/issues/9528), [#9529](https://github.com/angular/angular.js/issues/9529))
- **$injector:** ensure $get method invoked with provider context
  ([372fa699](https://github.com/angular/angular.js/commit/372fa6993b2b1b4848aa4be3c3e11f69244fca6f),
   [#9511](https://github.com/angular/angular.js/issues/9511), [#9512](https://github.com/angular/angular.js/issues/9512))
- **$location:** use clone of passed search() object
  ([c7a9009e](https://github.com/angular/angular.js/commit/c7a9009e143299f0e45a85d715ff22fc676d3f93),
   [#9445](https://github.com/angular/angular.js/issues/9445))
- **$parse:** stabilize one-time literal expressions correctly
  ([874cac82](https://github.com/angular/angular.js/commit/874cac825bf29a936cb1b35f9af239687bc5e036))
- **formController:** remove scope reference when form is destroyed
  ([01f50e1a](https://github.com/angular/angular.js/commit/01f50e1a7b2bff7070616494774ec493f8133204),
   [#9315](https://github.com/angular/angular.js/issues/9315))
- **jqLite:** remove native listener when all jqLite listeners were deregistered
  ([d71fb6f2](https://github.com/angular/angular.js/commit/d71fb6f2713f1a636f6e9c25479870ee9941ad18),
   [#9509](https://github.com/angular/angular.js/issues/9509))
- **select:**
  - add basic track by and select as support
  ([addfff3c](https://github.com/angular/angular.js/commit/addfff3c46311f59bdcd100351260006d457316f),
   [#6564](https://github.com/angular/angular.js/issues/6564))
  - manage select controller options correctly
  ([2435e2b8](https://github.com/angular/angular.js/commit/2435e2b8f84fde9495b8e9440a2b4f865b1ff541),
   [#9418](https://github.com/angular/angular.js/issues/9418))


## Features

- **$anchorScroll:** support a configurable vertical scroll offset
  ([09c39d2c](https://github.com/angular/angular.js/commit/09c39d2ce687cdf0ac35dbb34a91f0d198c9d83a),
   [#9368](https://github.com/angular/angular.js/issues/9368), [#2070](https://github.com/angular/angular.js/issues/2070), [#9360](https://github.com/angular/angular.js/issues/9360))
- **$animate:**
  - introduce the $animate.animate() method
  ([02be700b](https://github.com/angular/angular.js/commit/02be700bda191b454de393f2805916f374a1d764))
  - allow $animate to pass custom styles into animations
  ([e5f4d7b1](https://github.com/angular/angular.js/commit/e5f4d7b10ae5e6a17ab349995451c33b7d294245))
- **currencyFilter:** add fractionSize as optional parameter
  ([20685ffe](https://github.com/angular/angular.js/commit/20685ffe11036d4d604d13f0d792ca46497af4a1),
   [#3642](https://github.com/angular/angular.js/issues/3642), [#3461](https://github.com/angular/angular.js/issues/3461), [#3642](https://github.com/angular/angular.js/issues/3642), [#7922](https://github.com/angular/angular.js/issues/7922))
- **jqLite:** add private jqLiteDocumentLoaded function
  ([0dd316ef](https://github.com/angular/angular.js/commit/0dd316efea209e5e5de3e456b4e6562f011a1294))


## Breaking Changes

- **$animate:** due to [e5f4d7b1](https://github.com/angular/angular.js/commit/e5f4d7b10ae5e6a17ab349995451c33b7d294245),
  staggering animations that use transitions will now
always block the transition from starting (via `transition: 0s none`)
up until the stagger step kicks in. The former behaviour was that the
block was removed as soon as the pending class was added. This fix
allows for styles to be applied in the pending class without causing
an animation to trigger prematurely.



<a name="1.3.0-rc.5"></a>
# 1.3.0-rc.5 impossible-choreography (2014-10-08)


## Bug Fixes

- **$anchorScroll:** don't scroll to top when initializing and location hash is empty
  ([d5445c60](https://github.com/angular/angular.js/commit/d5445c601fafd6ecd38befeaa4c9ec7bb044127c),
   [#8848](https://github.com/angular/angular.js/issues/8848), [#9393](https://github.com/angular/angular.js/issues/9393))
- **$animate:**
  - ensure hidden elements with ngShow/ngHide stay hidden during animations
  ([39d0b368](https://github.com/angular/angular.js/commit/39d0b36826a077f7549a70d0cf3edebe90a10aaa),
   [#9103](https://github.com/angular/angular.js/issues/9103), [#9493](https://github.com/angular/angular.js/issues/9493))
  - permit class-based animations for leave operations if ngAnimateChildren is enabled
  ([df1a00b1](https://github.com/angular/angular.js/commit/df1a00b11ac2722f4da441837795985f12682030),
   [#8092](https://github.com/angular/angular.js/issues/8092), [#9491](https://github.com/angular/angular.js/issues/9491))
  - ensure that class-based animations only consider the most recent DOM operations
  ([c93924ed](https://github.com/angular/angular.js/commit/c93924ed275a62683b85c82f1c6c2e19d5662c9a),
   [#8946](https://github.com/angular/angular.js/issues/8946), [#9458](https://github.com/angular/angular.js/issues/9458))
  - abort class-based animations if the element is removed during digest
  ([613d0a32](https://github.com/angular/angular.js/commit/613d0a3212de8dc01c817ca8526e09c57978a621),
   [#8796](https://github.com/angular/angular.js/issues/8796))
  - clear the GCS cache even when no animation is detected
  ([cb85cbce](https://github.com/angular/angular.js/commit/cb85cbcec1c876db6062a0dc0bad80f842782194),
   [#8813](https://github.com/angular/angular.js/issues/8813))
- **$browser:**
  - Cache `location.href` only during page reload phase
  ([8ee1ba4b](https://github.com/angular/angular.js/commit/8ee1ba4b94d6fccff06d8781f7ed256c6ce664ff),
   [#9235](https://github.com/angular/angular.js/issues/9235), [#9455](https://github.com/angular/angular.js/issues/9455))
  - don’t use the history API when only the hash changes
  ([7cb01a80](https://github.com/angular/angular.js/commit/7cb01a80beec669d8f6aae1dc211d2f0b7d4eac4),
   [#9423](https://github.com/angular/angular.js/issues/9423), [#9424](https://github.com/angular/angular.js/issues/9424),
   [858360b6](https://github.com/angular/angular.js/commit/858360b680a2bb5c19429c1be1c9506700cda476),
   [0656484d](https://github.com/angular/angular.js/commit/0656484d3e709c5162570b0dd6473b0b6140e5b2),
   [#9143](https://github.com/angular/angular.js/issues/9143), [#9406](https://github.com/angular/angular.js/issues/9406))
  - handle async href on url change in <=IE9
  ([404b95fe](https://github.com/angular/angular.js/commit/404b95fe30a1bcd1313adafbd0018578d5b21d3d),
   [#9235](https://github.com/angular/angular.js/issues/9235))
- **$compile:**
  - handle the removal of an interpolated attribute
  ([a75546af](https://github.com/angular/angular.js/commit/a75546afdf41adab786eda30c258190cd4c5f1ae),
   [#9236](https://github.com/angular/angular.js/issues/9236), [#9240](https://github.com/angular/angular.js/issues/9240))
  - remove comment nodes from templates before asserting single root node
  ([feba0174](https://github.com/angular/angular.js/commit/feba0174db0f8f929273beb8b90691734a9292e2),
   [#9212](https://github.com/angular/angular.js/issues/9212), [#9215](https://github.com/angular/angular.js/issues/9215))
  - use the correct namespace for transcluded svg elements
  ([f3539f3c](https://github.com/angular/angular.js/commit/f3539f3cb5d9477f50f065c6a0ac7d6ca0a31092),
   [#9344](https://github.com/angular/angular.js/issues/9344), [#9415](https://github.com/angular/angular.js/issues/9415))
- **$http:** honor application/json response header and parse json primitives
  ([7b6c1d08](https://github.com/angular/angular.js/commit/7b6c1d08aceba6704a40302f373400aed9ed0e0b),
   [#2973](https://github.com/angular/angular.js/issues/2973))
- **$injector:** throw when factory $get method does not return a value
  ([0d3b69a5](https://github.com/angular/angular.js/commit/0d3b69a5f27b41745b504c7ffd8d72653bac1f85),
   [#4575](https://github.com/angular/angular.js/issues/4575), [#9210](https://github.com/angular/angular.js/issues/9210))
- **$location:** allow `0` in `path()` and `hash()`
  ([b8c5b871](https://github.com/angular/angular.js/commit/b8c5b87119a06edb8e8d1cefad81ee8d1f64f070))
- **form:** fix submit prevention
  ([86c7d122](https://github.com/angular/angular.js/commit/86c7d1221c706993044583d51a0c61423fee5bcf),
   [#3370](https://github.com/angular/angular.js/issues/3370), [#3776](https://github.com/angular/angular.js/issues/3776))
- **ngAnimate:** defer DOM operations for changing classes to postDigest
  ([667183a8](https://github.com/angular/angular.js/commit/667183a8c79d6ffce571a2be78c05dc76503b222),
   [#8234](https://github.com/angular/angular.js/issues/8234), [#9263](https://github.com/angular/angular.js/issues/9263))
- **orderBy:** sort by identity if no predicate is given
  ([607f016a](https://github.com/angular/angular.js/commit/607f016a0ba705ce40df0164360fb96a9d7f5912),
   [#5847](https://github.com/angular/angular.js/issues/5847), [#4579](https://github.com/angular/angular.js/issues/4579), [#9403](https://github.com/angular/angular.js/issues/9403))
- **select:**
  - throw for `selectAs` and `trackBy`
  ([30996f82](https://github.com/angular/angular.js/commit/30996f82afa03cd11771b3267e9367ecf9af6e6d))
  - use `$viewValue` instead of `$modelValue`
  ([f7174169](https://github.com/angular/angular.js/commit/f7174169f4f710d605f6a67f39f90a67a07d4cab),
   [#8929](https://github.com/angular/angular.js/issues/8929))


## Features

- **$location:**
  - add support for History API state handling ([6fd36dee](https://github.com/angular/angular.js/commit/6fd36deed954b338e48390862971d465148dc1f2),
   [#9027](https://github.com/angular/angular.js/issues/9027))
  - allow automatic rewriting of links to be disabled
  ([b3e09be5](https://github.com/angular/angular.js/commit/b3e09be58960b913fee3869bf36e7de3305bbe00),
   [#5487](https://github.com/angular/angular.js/issues/5487))
- **$route:** ability to cancel $routeChangeStart event
  ([f4ff11b0](https://github.com/angular/angular.js/commit/f4ff11b01e6a5f9a9eb25a38d327dfaadbd7c80c),
   [#5581](https://github.com/angular/angular.js/issues/5581), [#5714](https://github.com/angular/angular.js/issues/5714), [#9502](https://github.com/angular/angular.js/issues/9502))

## Performance Improvements

- **$animate:**
  - access DOM less in resolveElementClasses
  ([22358cf9](https://github.com/angular/angular.js/commit/22358cf9c703d67f3cf9eb4899404b09578a5fad))
  - don't join classes before it's necessary in resolveElementClasses
  ([003c44ec](https://github.com/angular/angular.js/commit/003c44eceee54c3398b0d2971fd97a512d7f7cec))
- **ngBind:** set textContent rather than using element.text()
  ([074a146d](https://github.com/angular/angular.js/commit/074a146d8b1ee7c93bf6d5892448a5c2a0143a28),
   [#9369](https://github.com/angular/angular.js/issues/9369), [#9396](https://github.com/angular/angular.js/issues/9396))


## Breaking Changes

- **$compile:** due to [feba0174](https://github.com/angular/angular.js/commit/feba0174db0f8f929273beb8b90691734a9292e2),


If a template contains directives within comment nodes, and there is more than a single node in the
template, those comment nodes are removed. The impact of this breaking change is expected to be
quite low.

Closes #9212
Closes #9215

- **ngAnimate:** due to [667183a8](https://github.com/angular/angular.js/commit/667183a8c79d6ffce571a2be78c05dc76503b222),


The `$animate` CSS class API will always defer changes until the end of the next digest. This allows ngAnimate
to coalesce class changes which occur over a short period of time into 1 or 2 DOM writes, rather than
many. This prevents jank in browsers such as IE, and is generally a good thing.

If you find that your classes are not being immediately applied, be sure to invoke `$digest()`.

Closes #8234
Closes #9263

- **$select:** due to [30996f8](https://github.com/angular/angular.js/commit/30996f82afa03cd11771b3267e9367ecf9af6e6d)

`ngOptions` will now throw an error when the comprehension expressions contains both a `select as`
and `track by` expression.

These expressions are fundamentally incompatible because it is not possible to reliably and
consistently determine the parent object of a model, since `select as` can assign any child of a
`value` as the model value.

Prior to refactorings in this release, neither of these expressions worked correctly independently,
and did not work at all when combined.

See #6564

- **$route:** due to [f4ff11b0](https://github.com/angular/angular.js/commit/f4ff11b01e6a5f9a9eb25a38d327dfaadbd7c80c),

Order of events has changed.
Previously: `$locationChangeStart` -> `$locationChangeSuccess`
  -> `$routeChangeStart` -> `$routeChangeSuccess`

Now: `$locationChangeStart` -> `$routeChangeStart`
  -> `$locationChangeSuccess` ->  -> `$routeChangeSuccess`

Fixes #5581
Closes #5714
Closes #9502


<a name="1.3.0-rc.4"></a>
# 1.3.0-rc.4 unicorn-hydrafication (2014-10-01)


## Bug Fixes

- **$compile:**
  - get $$observe listeners array as own property
  ([a27d827c](https://github.com/angular/angular.js/commit/a27d827c22b0b6b3ba6b7495cf4fc338c6934b37),
   [#9343](https://github.com/angular/angular.js/issues/9343), [#9345](https://github.com/angular/angular.js/issues/9345))
  - Resolve leak with asynchronous compilation
  ([6303c3dc](https://github.com/angular/angular.js/commit/6303c3dcf64685458fc84aa12289f5c9d57f4e47),
   [#9199](https://github.com/angular/angular.js/issues/9199), [#9079](https://github.com/angular/angular.js/issues/9079), [#8504](https://github.com/angular/angular.js/issues/8504), [#9197](https://github.com/angular/angular.js/issues/9197))
  - connect transclude scopes to their containing scope to prevent memory leaks
  ([fb0c77f0](https://github.com/angular/angular.js/commit/fb0c77f0b66ed757a56af13f81b943419fdcbd7f),
   [#9095](https://github.com/angular/angular.js/issues/9095), [#9281](https://github.com/angular/angular.js/issues/9281))
  - sanitize srcset attribute
  ([ab80cd90](https://github.com/angular/angular.js/commit/ab80cd90661396dbb1c94c5f4dd2d11ee8f6b6af))
- **input:**
  - register builtin parsers/formatters before anyone else
  ([10644432](https://github.com/angular/angular.js/commit/10644432ca9d5da69ce790a8d9e691640f333711),
   [#9218](https://github.com/angular/angular.js/issues/9218), [#9358](https://github.com/angular/angular.js/issues/9358))
  - correctly handle invalid model values for `input[date/time/…]`
  ([a0bfdd0d](https://github.com/angular/angular.js/commit/a0bfdd0d60882125f614a91c321f12f730735e7b),
   [#8949](https://github.com/angular/angular.js/issues/8949), [#9375](https://github.com/angular/angular.js/issues/9375))
- **ngModel:** do not parse undefined viewValue when validating
  ([92f05e5a](https://github.com/angular/angular.js/commit/92f05e5a5900713301e64373d7b7daa45a88278b),
   [#9106](https://github.com/angular/angular.js/issues/9106), [#9260](https://github.com/angular/angular.js/issues/9260))
- **ngView:** use animation promises ensure that only one leave animation occurs at a time
  ([3624e380](https://github.com/angular/angular.js/commit/3624e3800fb3ccd2e9ea361a763e20131fd42c29),
   [#9355](https://github.com/angular/angular.js/issues/9355), [#7606](https://github.com/angular/angular.js/issues/7606), [#9374](https://github.com/angular/angular.js/issues/9374))
- **select:** make ctrl.hasOption method consistent
  ([2bcd02dc](https://github.com/angular/angular.js/commit/2bcd02dc1a6b28b357d47c83be3bed5c9a38417c),
   [#8761](https://github.com/angular/angular.js/issues/8761))


## Features

- **$compile:** optionally get controllers from ancestors only
  ([07e3abc7](https://github.com/angular/angular.js/commit/07e3abc7dda872adc3fb25cb3e133f86f494b35d),
   [#4518](https://github.com/angular/angular.js/issues/4518), [#4540](https://github.com/angular/angular.js/issues/4540), [#8240](https://github.com/angular/angular.js/issues/8240), [#8511](https://github.com/angular/angular.js/issues/8511))
- **Scope:** allow the parent of a new scope to be specified on creation
  ([6417a3e9](https://github.com/angular/angular.js/commit/6417a3e9eb7ab0011cefada8db855aa929a64ff8))


## Performance Improvements

- **$rootScope:** moving internal queues out of the Scope instances
  ([b1192518](https://github.com/angular/angular.js/commit/b119251827cea670051198e1b48af7ee0c9f2a1b),
   [#9071](https://github.com/angular/angular.js/issues/9071))
- **benchmark:** add ngBindOnce benchmarks to largetable-bp
  ([2c8b4648](https://github.com/angular/angular.js/commit/2c8b4648526acf5c2645de8408a6d9ace2144b5f))
- **ngForm,ngModel:** move initial addClass to the compile phase
  ([b1ee5386](https://github.com/angular/angular.js/commit/b1ee5386d584f208bce6d3b613afdb3bae9df76a),
   [#8268](https://github.com/angular/angular.js/issues/8268))


## Breaking Changes

- **$compile:** due to [fb0c77f0](https://github.com/angular/angular.js/commit/fb0c77f0b66ed757a56af13f81b943419fdcbd7f),


`$transclude` functions no longer attach `$destroy` event handlers to the
transcluded content, and so the associated transclude scope will not automatically
be destroyed if you remove a transcluded element from the DOM using direct DOM
manipulation such as the jquery `remove()` method.

If you want to explicitly remove DOM elements inside your directive that have
been compiled, and so potentially contain child (and transcluded) scopes, then
it is your responsibility to get hold of the scope and destroy it at the same time.

The suggested approach is to create a new child scope of your own around any DOM
elements that you wish to manipulate in this way and destroy those scopes if you
remove their contents - any child scopes will then be destroyed and cleaned up
automatically.

Note that all the built-in directives that manipulate the DOM (ngIf, ngRepeat,
ngSwitch, etc) already follow this best practice, so if you only use these for
manipulating the DOM then you do not have to worry about this change.

Closes #9095
Closes #9281

- **$parse:** due to [5572b40b](https://github.com/angular/angular.js/commit/5572b40b15ed06969c8e0e92866c5afd088484b4),

- $scope['this'] no longer exits on the $scope object
- $parse-ed expressions no longer allow chaining 'this' such as this['this'] or $parent['this']
- 'this' in $parse-ed expressions can no longer be overriden, if a variable named 'this' is put on the scope it must be accessed using this['this']

Closes #9105

- **input:** due to [1eda1836](https://github.com/angular/angular.js/commit/1eda18365a348c9597aafba9d195d345e4f13d1e),

(Note: this change landed in 1.3.0-rc.3, but was not considered a breaking change at the time).

For text based inputs (text, email, url), the `$viewValue` will now always be converted to a string,
regardless of what type the value is on the model.

To migrate, any code or expressions that expect the `$viewValue` to be anything other than string
should be updated to expect a string.


- **input:** due to a0bfdd0d60882125f614a91c321f12f730735e7b (see #8949),

Similar to `input[number]` Angular will now throw if the model value
for a `input[date]` is not a `Date` object. Previously, Angular only
showed an empty string instead.
Angular does not set validation errors on the `<input>` in this case
as those errors are shown to the user, but the erroneous state was
caused by incorrect application logic and not by the user.


<a name="1.3.0-rc.3"></a>
# 1.3.0-rc.3 aggressive-pacification (2014-09-23)


## Bug Fixes

- **ngModel:** support milliseconds in time and datetime
  ([4b83f6ca](https://github.com/angular/angular.js/commit/4b83f6ca2c15bd65fe2b3894a02c04f9967fbff4),
   [#8874](https://github.com/angular/angular.js/issues/8874))


## Features

- **$location:** add ability to opt-out of `<base>` tag requirement in html5Mode
  ([dc3de7fb](https://github.com/angular/angular.js/commit/dc3de7fb7a14c38b5c3dc7decfafb0b51d422dd1),
   [#8934](https://github.com/angular/angular.js/issues/8934))
- **formController:** add $setUntouched to propagate untouched state
  ([fd899755](https://github.com/angular/angular.js/commit/fd8997551f9ed4431f5e99d61f637139485076b9),
   [#9050](https://github.com/angular/angular.js/issues/9050))
- **input:** support dynamic element validation
  ([729c238e](https://github.com/angular/angular.js/commit/729c238e19ab27deff01448d79342ea53721bfed),
   [#4791](https://github.com/angular/angular.js/issues/4791), [#1404](https://github.com/angular/angular.js/issues/1404))
- **ngAria:** add an ngAria module to make a11y easier
  ([d1434c99](https://github.com/angular/angular.js/commit/d1434c999a66c6bb915ee1a8b091e497d288d940),
   [#5486](https://github.com/angular/angular.js/issues/5486))


## Performance Improvements

- **map:** use Array.prototype.map
  ([a591e8b8](https://github.com/angular/angular.js/commit/a591e8b8d302efefd67bf0d5c4bad300a5f3aded))


## Breaking Changes

- **$location:** due to [dc3de7fb](https://github.com/angular/angular.js/commit/dc3de7fb7a14c38b5c3dc7decfafb0b51d422dd1),
  The $location.html5Mode API has changed to allow enabling html5Mode by
    passing an object (as well as still supporting passing a boolean). Symmetrically, the
    method now returns an object instead of a boolean value.

    To migrate, follow the code example below:

    Before:

    var mode = $locationProvider.html5Mode();

    After:

    var mode = $locationProvider.html5Mode().enabled;

Fixes #8934



<a name="1.3.0-rc.2"></a>
# 1.3.0-rc.2 tactile-perception (2014-09-16)


## Bug Fixes

- **$compile:** update `'@'`-bindings in controller when `bindToController` is `true`
  ([e7ac08a0](https://github.com/angular/angular.js/commit/e7ac08a0619d2bdc91c125d341772b4fbc0d5a78),
   [#9052](https://github.com/angular/angular.js/issues/9052), [#9077](https://github.com/angular/angular.js/issues/9077))
- **$parse:** ensure CSP assignable expressions have `assign()`
  ([d13b4bd1](https://github.com/angular/angular.js/commit/d13b4bd1f5f2abaad00f5d1bf81f79549a8d0e46),
   [#9048](https://github.com/angular/angular.js/issues/9048))
- **i18n:** fix typo at i18n generation code
  ([eb4afd45](https://github.com/angular/angular.js/commit/eb4afd45f77d7d67744e01ce63a831c13c2b22e8))
- **input:** always pass in the model value to `ctrl.$isEmpty`
  ([3e51b84b](https://github.com/angular/angular.js/commit/3e51b84bc19f7e6acc61cb536ddcdbfed307c831),
   [#5164](https://github.com/angular/angular.js/issues/5164), [#9017](https://github.com/angular/angular.js/issues/9017))
- **jqLite:** fix `event.stopImmediatePropagation()` so it works as expected
  ([30354c58](https://github.com/angular/angular.js/commit/30354c58fe2bd371df364f7a3f55b270692a4051),
   [#4833](https://github.com/angular/angular.js/issues/4833))
- **ngLocale:** Regenerate Locale Files
  ([6a96a820](https://github.com/angular/angular.js/commit/6a96a8200aff4749bc84c44a1e8018b09d9ebdb4),
   [#8931](https://github.com/angular/angular.js/issues/8931), [#8583](https://github.com/angular/angular.js/issues/8583), [#7799](https://github.com/angular/angular.js/issues/7799))
- **ngModel:**
  - do not reset bound date objects
  ([1a1ef629](https://github.com/angular/angular.js/commit/1a1ef62903c8fdf4ceb81277d966a8eff67f0a96),
   [#6666](https://github.com/angular/angular.js/issues/6666))
  - don’t clear the model when an external validator failed
  ([9314719d](https://github.com/angular/angular.js/commit/9314719d1eb5f480b877f5513f6e0e474edcb67d),
   [#8357](https://github.com/angular/angular.js/issues/8357), [#8080](https://github.com/angular/angular.js/issues/8080))
- **ngResource:** make badcfg error message more helpful
  ([a3962f0d](https://github.com/angular/angular.js/commit/a3962f0df3f9b8382b47952f9e4fcb48a4cc098b),
   [#9005](https://github.com/angular/angular.js/issues/9005), [#9010](https://github.com/angular/angular.js/issues/9010))
- **select:** update option labels when model changes
  ([46274102](https://github.com/angular/angular.js/commit/46274102454038ee7fd4543a32166e9bbbc98904),
   [#9025](https://github.com/angular/angular.js/issues/9025))


## Features

- **limitTo:** support numeric input to limitTo
  ([1c8a7459](https://github.com/angular/angular.js/commit/1c8a7459c90efc77b1a0987f976e3bddab4565fe),
   [#8926](https://github.com/angular/angular.js/issues/8926))
- **ngInclude:** add template url parameter to events
  ([fd2d6c02](https://github.com/angular/angular.js/commit/fd2d6c02f9654e753d3655a3377a9534f7a54de3),
   [#8453](https://github.com/angular/angular.js/issues/8453), [#8454](https://github.com/angular/angular.js/issues/8454))


## Performance Improvements

- **$compile:** move `$$isolateBinding` creation to directive factory instead of on each link
  ([56f09f0b](https://github.com/angular/angular.js/commit/56f09f0b44048b62f964d29db4d3d2630662f6ea))
- **$parse:**
  - execute watched expressions only when the inputs change
  ([fca6be71](https://github.com/angular/angular.js/commit/fca6be71274e537c7df86ae9e27a3bd1597e9ffa),
   [#9006](https://github.com/angular/angular.js/issues/9006), [#9082](https://github.com/angular/angular.js/issues/9082))
  - remove `binaryFn` and `valueFn` wrappers from filter expressions
  ([67919c80](https://github.com/angular/angular.js/commit/67919c808771a9b185a9d552cd32a90748d36666))


## Breaking Changes

- **$parse:** due to [fca6be71](https://github.com/angular/angular.js/commit/fca6be71274e537c7df86ae9e27a3bd1597e9ffa),
  all filters are assumed to be stateless functions

Previously it was just a good practice to make all filters stateless. Now
it's a requirement in order for the model change-observation to pick up
all changes.

If an existing filter is statefull, it can be flagged as such but keep in
mind that this will result in a significant performance-penalty (or rather
lost opportunity to benefit from a major perf improvement) that will
affect the `$digest` duration.

To flag a filter as stateful do the following:

```javascript
myApp.filter('myFilter', function() {
  function myFilter(input) { ... };
  myFilter.$stateful = true;
  return myFilter;
});
```



<a name="1.3.0-rc.1"></a>
# 1.3.0-rc.1 backyard-atomicity (2014-09-09)


## Bug Fixes

- **$location:**
  - don't call toString on null values
  ([c3a58a9f](https://github.com/angular/angular.js/commit/c3a58a9f34919f121587540e03ecbd51b25198d4))
  - remove an unused parameter of $location.url
  ([99d95f16](https://github.com/angular/angular.js/commit/99d95f1639b64c39231448d77209676b54e6f0be))
  - allow numeric location setter arguments
  ([adb5c6d6](https://github.com/angular/angular.js/commit/adb5c6d6cc76b928436743707727ab0974d6810b),
   [#7054](https://github.com/angular/angular.js/issues/7054))
  - set `baseHref` in mock browser to `/`
  ([fc706d13](https://github.com/angular/angular.js/commit/fc706d13d80bb40eb3dade58ea4b92dca33ce4e7),
   [#8866](https://github.com/angular/angular.js/issues/8866), [#8889](https://github.com/angular/angular.js/issues/8889))
- **$parse:** disallow passing Function to Array.sort
  ([bd8ad0fb](https://github.com/angular/angular.js/commit/bd8ad0fbe81f6c280baa26a596d78e58fc7842e6))
- **input:** check `scope.$$phase` only on `$rootScope`
  ([bf59d727](https://github.com/angular/angular.js/commit/bf59d7274f4a667c5b19e6d4ba5ed2730ca2fe42))
- **ngAnimate:** support removing classes from SVG elements when using jQuery
  ([b3b67213](https://github.com/angular/angular.js/commit/b3b672130d4d1c6f13bdf7e58be76b2aafea2497),
   [#8872](https://github.com/angular/angular.js/issues/8872), [#8893](https://github.com/angular/angular.js/issues/8893))
- **ngEventDirs:** check `scope.$$phase` only on `$rootScope`
  ([203ea10f](https://github.com/angular/angular.js/commit/203ea10f9ea49d7e29569a4232d3b2a666307cd8),
   [#8891](https://github.com/angular/angular.js/issues/8891))
- **ngForm:** don't clear validity of whole form when removing control
  ([953ee22f](https://github.com/angular/angular.js/commit/953ee22f76f8c1137949ed07f36fafc5bbfeb7fe),
   [#8863](https://github.com/angular/angular.js/issues/8863))
- **ngInclude:** correctly add svg-namespaced template content
  ([6639ca9d](https://github.com/angular/angular.js/commit/6639ca9d6bc00a6e3a31e54c50474361ae3561c6),
   [#7538](https://github.com/angular/angular.js/issues/7538), [#8981](https://github.com/angular/angular.js/issues/8981), [#8997](https://github.com/angular/angular.js/issues/8997))
- **ngModel:**
  - update model value with async validators correctly
  ([64c3b745](https://github.com/angular/angular.js/commit/64c3b745fba0792166f30e057f9251f263d80dac))
  - render immediately also with async validators
  ([f94d5515](https://github.com/angular/angular.js/commit/f94d551529b7c970c38b29e3073cec4e7f6b0e00))
  - properly parse min/max date values as strings for date inputs
  ([088545c1](https://github.com/angular/angular.js/commit/088545c1856ce1c3ec3416965dff65077a6e0523),
   [#6755](https://github.com/angular/angular.js/issues/6755))
  - revalidate the model when min/max expression values change for date inputs
  ([b3502835](https://github.com/angular/angular.js/commit/b3502835039178296b730b7526e5666b66ba9156),
   [#6755](https://github.com/angular/angular.js/issues/6755))
  - consider ngMin/ngMax values when validating number input types
  ([25541c1f](https://github.com/angular/angular.js/commit/25541c1f876a16c892d71faae11727bec7bba98c))
  - revalidate the model when min/max expression values change for number inputs
  ([7b273a2c](https://github.com/angular/angular.js/commit/7b273a2c978d5f5ef374f5335afab0ca7d8cfd4d),
   [#2404](https://github.com/angular/angular.js/issues/2404))
- **ngModelOptions:** do not trigger digest on `setViewValue` if debouncing
  ([e322cd9b](https://github.com/angular/angular.js/commit/e322cd9b3b8b47b95c9de3edf631bb46f919c492),
   [#8814](https://github.com/angular/angular.js/issues/8814), [#8850](https://github.com/angular/angular.js/issues/8850), [#8911](https://github.com/angular/angular.js/issues/8911))
- **ngRepeat:** preserve original position of elements that are being animated away
  ([ed637330](https://github.com/angular/angular.js/commit/ed6373300028deda9a0878b3975699d183c1f75c),
   [#8918](https://github.com/angular/angular.js/issues/8918), [#8994](https://github.com/angular/angular.js/issues/8994))
- **ngSwitch:** ensure correct iterator is passed to async function
  ([712299c2](https://github.com/angular/angular.js/commit/712299c2a24390e74cd5c20f51cb1d78f0233b6f),
   [#8833](https://github.com/angular/angular.js/issues/8833))
- **numberFilter:** format numbers that round to zero as nonnegative
  ([ae952fbf](https://github.com/angular/angular.js/commit/ae952fbf0be925a48743d1c925ffe4e31a42c280),
   [#8489](https://github.com/angular/angular.js/issues/8489))
- **orderBy:** allow arrayLike objects to be ordered
  ([cbdaabfb](https://github.com/angular/angular.js/commit/cbdaabfb59bf3348588d5b581f2754e0f9f034a4),
   [#8944](https://github.com/angular/angular.js/issues/8944))


## Features

- **angular.forEach:** add the array/object as the 3rd param like the native array forEach
  ([df9e60c8](https://github.com/angular/angular.js/commit/df9e60c8e7453cdca2cb5a4fa48f3981ecc23a7d),
   [#7902](https://github.com/angular/angular.js/issues/7902))
- **ngModelOptions:** add allowInvalid option
  ([3c538c1d](https://github.com/angular/angular.js/commit/3c538c1d21c43422c7b4cd9b69cb67981bce2b87),
   [#8290](https://github.com/angular/angular.js/issues/8290), [#8313](https://github.com/angular/angular.js/issues/8313))


## Performance Improvements

- **$parse:**
  - remove getterFn wrapper for internal use
  ([b3b476db](https://github.com/angular/angular.js/commit/b3b476db7d34bc2f8b099ab5b993b1e899b9cffd),
   [#8901](https://github.com/angular/angular.js/issues/8901))
  - removing references to Parser/Lexer from parsed expressions
  ([43c67ccd](https://github.com/angular/angular.js/commit/43c67ccd167aecc3549e1b7f7d100956204e3ed4))
  - calculate array lengths once at start of loop
  ([907b8c16](https://github.com/angular/angular.js/commit/907b8c1675865ac38dd055f3f304272e68b233d0))
- **extend:** remove use of forEach to remove calls/closures/passing arguments
  ([9bedeb33](https://github.com/angular/angular.js/commit/9bedeb3353969fba631ad9164edea3c38059fbda),
   [#8898](https://github.com/angular/angular.js/issues/8898))
- **jQuery:** only trigger $destroy if a handler exists
  ([f6aa1c55](https://github.com/angular/angular.js/commit/f6aa1c55616b34215f562e0445e436210860ef04),
   [#8859](https://github.com/angular/angular.js/issues/8859))


## Breaking Changes

- **ngModelController,formController:** due to [6046e14b](https://github.com/angular/angular.js/commit/6046e14bd22491168116e61ffdf5fd3fed5f135c),

- `ctrl.$error` no longer contains entries for validators that were
  successful.
- `ctrl.$setValidity` now differentiates between `true`, `false`,
  `undefined` and `null`, instead of previously only truthy vs falsy.

Closes #8941- **ngSwitch:** due to [0f806d96](https://github.com/angular/angular.js/commit/0f806d9659b5b89a4bd9493364bc36398677e939),


Ever since 0df93fd, tagged in v1.0.0rc1, the ngSwitch directive has had an undocumented `change`
attribute, used for evaluating a scope expression when the switch value changes.

While it's unlikely, applications which may be using this feature should work around the removal
by adding a custom directive which will perform the eval instead. Directive controllers are
re-instantiated when being transcluded, so by putting the attribute on each item that you want
to be notified of a change to, you can more or less emulate the old behaviour.

Example:

```js
angular.module("switchChangeWorkaround", []).
  directive("onSwitchChanged", function() {
    return {
      link: function($scope, $element, $attrs) {
        $scope.$parent.$eval($attrs.onSwitchChanged);
      }
    };
  });
```

```html
<div ng-switch="switcher">
  <div ng-switch-when="a" on-switch-changed="doSomethingInParentScope()"></div>
  <div ng-switch-when="b" on-switch-changed="doSomethingInParentScope()"></div>
</div>
```

Closes #8858
Closes #8822



<a name="1.3.0-RC.0"></a>
# 1.3.0-RC.0 sonic-boltification (2014-08-29)


## Bug Fixes

- **$animate:**
  - wait two until two digests are over until enabling animations
  ([92576743](https://github.com/angular/angular.js/commit/92576743eec0cef5ffdd701b83f72a61e6489c3b),
   [#8844](https://github.com/angular/angular.js/issues/8844))
  - ensure guarded animations consider AJAX requests upon bootstrap
  ([4bca4c44](https://github.com/angular/angular.js/commit/4bca4c44b95a7435722605a750804043f2960160),
   [#8275](https://github.com/angular/angular.js/issues/8275), [#5262](https://github.com/angular/angular.js/issues/5262))
  - use $timeout to handle the delay within staggering animations
  ([23da6140](https://github.com/angular/angular.js/commit/23da614043fe5dcf0be132b86466eecb11c766a2),
   [#7228](https://github.com/angular/angular.js/issues/7228), [#7547](https://github.com/angular/angular.js/issues/7547), [#8297](https://github.com/angular/angular.js/issues/8297), [#8547](https://github.com/angular/angular.js/issues/8547))
- **$browser:** detect changes to the browser url that happened in sync
  ([3be00df4](https://github.com/angular/angular.js/commit/3be00df495f6eed3b3d9587ebab1fdd633e94e08),
   [#6976](https://github.com/angular/angular.js/issues/6976))
- **$compile:** use the correct namespace for transcluded svg elements
  ([cb73a37c](https://github.com/angular/angular.js/commit/cb73a37c7cae5cdebadf7b3ddd44c5a452495e4e),
   [#8808](https://github.com/angular/angular.js/issues/8808), [#8816](https://github.com/angular/angular.js/issues/8816))
- **$location:** always resolve relative links in html5mode to `<base>` url
  ([22948807](https://github.com/angular/angular.js/commit/22948807e324eb0b182b15b31045dc306a9f3231),
   [#8492](https://github.com/angular/angular.js/issues/8492), [#8172](https://github.com/angular/angular.js/issues/8172))
- **$parse:** properly handle dots at the end of identifiers
  ([8ac90357](https://github.com/angular/angular.js/commit/8ac90357a66ae0c62dbfe6db2c6eaf1d600ecc65),
   [#4613](https://github.com/angular/angular.js/issues/4613), [#4912](https://github.com/angular/angular.js/issues/4912), [#8559](https://github.com/angular/angular.js/issues/8559))
- **Angular:** remove duplicate nodeName_ references
  ([a4520a74](https://github.com/angular/angular.js/commit/a4520a745d917c77f1d12cdbce48272c643f7255))
- **currencyFilter:** pass through null and undefined values
  ([c2aaddbe](https://github.com/angular/angular.js/commit/c2aaddbe4b21348aab8c13a78cdd6aaee846ae4e),
   [#8605](https://github.com/angular/angular.js/issues/8605))
- **docs:** don't throw exception on the 404 page
  ([550ba01b](https://github.com/angular/angular.js/commit/550ba01b325fc29460030fc9c24fa00269dec2a9),
   [#8518](https://github.com/angular/angular.js/issues/8518))
- **input:**
  - validate minlength/maxlength for non-string values
  ([77ce5b89](https://github.com/angular/angular.js/commit/77ce5b89f97aa83c3eb1fe2e19375ef00a822015),
   [#7967](https://github.com/angular/angular.js/issues/7967), [#8811](https://github.com/angular/angular.js/issues/8811))
  - allow to use seconds in `input[time]` and `input[datetime-local]`
  ([5f90340a](https://github.com/angular/angular.js/commit/5f90340abb78aa08dde4876328bcc00e46232e46))
  - use year 1970 instead of 1900 for `input[time]`
  ([29f0b568](https://github.com/angular/angular.js/commit/29f0b568debab7810752969d363d337099e96cdc))
- **ngBindHtml:** throw error if interpolation is used in expression
  ([cd21602d](https://github.com/angular/angular.js/commit/cd21602d5b1650d8be373618cb7320d697e32c4d),
   [#8824](https://github.com/angular/angular.js/issues/8824))
- **ngEventDirs:** execute `blur` and `focus` expression using `scope.$evalAsync`
  ([719c747c](https://github.com/angular/angular.js/commit/719c747cd892ee933e7e414a7dc97e657b88317d),
   [#4979](https://github.com/angular/angular.js/issues/4979), [#5945](https://github.com/angular/angular.js/issues/5945), [#8803](https://github.com/angular/angular.js/issues/8803), [#6910](https://github.com/angular/angular.js/issues/6910), [#5402](https://github.com/angular/angular.js/issues/5402))
- **ngModel:**
  - always format the viewValue as a string for text, url and email types
  ([1eda1836](https://github.com/angular/angular.js/commit/1eda18365a348c9597aafba9d195d345e4f13d1e))
  - allow non-assignable binding when getterSetter is used
  ([ab878a6c](https://github.com/angular/angular.js/commit/ab878a6c038f47b95f3a7e85a4fdb599e0c73e63),
   [#8704](https://github.com/angular/angular.js/issues/8704))
  - treat undefined parse responses as parse errors
  ([db044c40](https://github.com/angular/angular.js/commit/db044c408a7f8082758b96ab739348810c36e15a))
- **ngRepeat:** improve errors for duplicate items
  ([0604bb7b](https://github.com/angular/angular.js/commit/0604bb7b7a6156e33679396e805e327662d9a178))
- **ngSwitch:** avoid removing DOM nodes twice within watch operation
  ([c9b0bfec](https://github.com/angular/angular.js/commit/c9b0bfecc99837af1c97792b3ca3408ba182b0bb),
   [#8662](https://github.com/angular/angular.js/issues/8662))
- **numberFilter:** pass through null and undefined values
  ([2ae10f67](https://github.com/angular/angular.js/commit/2ae10f67fcde3e172f695956301ef796b68a50c2),
   [#8605](https://github.com/angular/angular.js/issues/8605), [#8842](https://github.com/angular/angular.js/issues/8842))


## Features

- **core:**
  - add angular.reloadWithDebugInfo()
  ([41c1b88](https://github.com/angular/angular.js/commit/41c1b8858f02c7310bfabdd545ebb28e90eb4258))
- **$animate:**
  - use promises instead of callbacks for animations
  ([bf0f5502](https://github.com/angular/angular.js/commit/bf0f5502b1bbfddc5cdd2f138efd9188b8c652a9))
  - coalesce concurrent class-based animations within a digest loop
  ([2f4437b3](https://github.com/angular/angular.js/commit/2f4437b3a149eafb899f25933bd6c713b167d10e))
- **$compile:**
  - bind isolate scope properties to controller
  ([5f3f25a1](https://github.com/angular/angular.js/commit/5f3f25a1a6f9d4f2a66e2700df3b9c5606f1c255),
   [#7635](https://github.com/angular/angular.js/issues/7635), [#7645](https://github.com/angular/angular.js/issues/7645))
  - allow disabling scope info
  ([a1e5cd5f](https://github.com/angular/angular.js/commit/a1e5cd5fe3906ebee8c400247a1f793d3e2239fb))
- **$compile/ngBind:** allow disabling binding info
  ([3660fd09](https://github.com/angular/angular.js/commit/3660fd0912d3ccf6def8c9f02d8d4c0621c8d91f))
- **$http:** implement mechanism for coalescing calls to $apply in $http
  ([ea6fc6e6](https://github.com/angular/angular.js/commit/ea6fc6e69c2a2aa213c71ed4e917a0d54d064e4c),
   [#8736](https://github.com/angular/angular.js/issues/8736), [#7634](https://github.com/angular/angular.js/issues/7634), [#5297](https://github.com/angular/angular.js/issues/5297))
- **$rootScope:** implement $applyAsync to support combining calls to $apply into a single digest.
  ([e94d454b](https://github.com/angular/angular.js/commit/e94d454b840f6cc55a440741382b407836ad245b))
- **$templateRequest:** introduce the $templateRequest service
  ([a70e2833](https://github.com/angular/angular.js/commit/a70e2833ea276107b11aafea96ef4a6724ad4d83))
- **filter:** allow to define the timezone for formatting dates
  ([4739b1d9](https://github.com/angular/angular.js/commit/4739b1d9daebfd094b6181c5f2cb52ff71e31c61))
- **filterFilter:** pass index to function predicate
  ([46343c60](https://github.com/angular/angular.js/commit/46343c603db6192daf5303b92eb664749326c7e6),
   [#654](https://github.com/angular/angular.js/issues/654))
- **input:** allow to define the timezone for parsing dates
  ([cc6fc199](https://github.com/angular/angular.js/commit/cc6fc199f5abaacdf781aa03634337d776eb0fc9),
   [#8447](https://github.com/angular/angular.js/issues/8447))
- **minErr:** allow specifying ErrorConstructor in minErr constructor
  ([a6bd4bc8](https://github.com/angular/angular.js/commit/a6bd4bc866a18f860c7548fa1b3f6d4c2a953416))
- **ngModel:** provide validation API functions for sync and async validations
  ([2ae4f40b](https://github.com/angular/angular.js/commit/2ae4f40be1803d999ca2a8cc30ec17ff19ea6d86))
- **ngRoute:** alias string as redirectTo property in .otherwise()
  ([3b5d75c0](https://github.com/angular/angular.js/commit/3b5d75c021e21fa6ec4dc6c47b8eafa55680ea63),
   [#7794](https://github.com/angular/angular.js/issues/7794))
- **testability:** add $$testability service
  ([85880a64](https://github.com/angular/angular.js/commit/85880a64900fa22a61feb926bf52de0965332ca5))


## Performance Improvements

- **$compile:**
  - add debug classes in compile phase
  ([e0489abd](https://github.com/angular/angular.js/commit/e0489abd8d9e4971ae23cc38805a92d227d1f3a1))
  - only iterate over elements with link functions
  ([fdf9989f](https://github.com/angular/angular.js/commit/fdf9989f7cf1ed81982a788b75a338ac33334571),
   [#8741](https://github.com/angular/angular.js/issues/8741))
- **nodeName_:** simplify the code and reduce the number of DOM calls
  ([5a1a0c96](https://github.com/angular/angular.js/commit/5a1a0c96220101b5e040f0755e5eb401e2c73f65))
- **select:** execute render after $digest cycle
  ([6f7018d5](https://github.com/angular/angular.js/commit/6f7018d52fa4f9f9c7fa8e3035317d1239efb20f),
   [#8825](https://github.com/angular/angular.js/issues/8825))


## Breaking Changes

- **$location**: due to [22948807](https://github.com/angular/angular.js/commit/22948807e324eb0b182b15b31045dc306a9f3231)

#### since 1.2.0 and 1.3.0-beta.1

Angular now requires a `<base>` tag when html5 mode of `$location` is enabled. Reasoning:
Using html5 mode without a `<base href="...">` tag makes relative links for images, links, ...
relative to the current url if the browser supports
the history API. However, if the browser does not support the history API Angular falls back to using the `#`,
and then all those relative links would be broken.

The `<base>` tag is also needed when a deep url is loaded from the server, e.g. `http://server/some/page/url`.
In that case, Angular needs to decide which part of the url is the base of the application, and which part
is path inside of the application.

To summarize: Now all relative links are always relative to the `<base>` tag.

Exception (also a breaking change):
Link tags whose `href` attribute starts with a `#` will only change the hash of the url, but nothing else
(e.g. `<a href="#someAnchor">`). This is to make it easy to scroll to anchors inside a document.

Related to #6162
Closes #8492

#### since 1.2.17 and 1.3.0-beta.10

In html5 mode without a `<base>` tag on older browser that don't support the history API
relative paths were adding up. E.g. clicking on `<a href="page1">` and then on `<a href="page2">`
would produce `$location.path()==='/page1/page2'`. The code that introduced this behavior was removed
and Angular now also requires a `<base>` tag to be present when using html5 mode.

Closes #8172, #8233


- **ngInclude, ngMessage, ngView and directives that load templates**: due to [a70e2833](https://github.com/angular/angular.js/commit/a70e2833ea276107b11aafea96ef4a6724ad4d83)

Angular will now throw a $compile minErr each a template fails to download
for ngView, directives and ngMessage template requests. This changes the former
behavior of silently ignoring failed HTTP requests--or when the template itself
is empty. Please ensure that all directive, ngView and ngMessage code now properly
addresses this scenario. NgInclude is uneffected from this change.


- **$animate**: due to [23da6140](https://github.com/angular/angular.js/commit/23da614043fe5dcf0be132b86466eecb11c766a2)

If any stagger code consisted of having BOTH transition staggers and delay staggers
together then that will not work the same way. Angular will now instead choose
the highest stagger delay value and set the timeout to wait for that before
applying the active CSS class.


- **$animate**: due to [bf0f5502](https://github.com/angular/angular.js/commit/bf0f5502b1bbfddc5cdd2f138efd9188b8c652a9)

Both the API for the cancallation method and the done callback for
$animate animations is different. Instead of using a callback function
for each of the $animate animation methods, a promise is used instead.

```js
//before
$animate.enter(element, container, null, callbackFn);

//after
$animate.enter(element, container).then(callbackFn);
```

The animation can now be cancelled via `$animate.cancel(promise)`.

```js
//before
var cancelFn = $animate.enter(element, container);
cancelFn(); //cancels the animation

//after
var promise = $animate.enter(element, container);
$animate.cancel(promise); //cancels the animation
```

keep in mind that you will still need to run $scope.$apply inside of the `then` callback
to trigger a digest.


- **$animate**: due to [2f4437b3](https://github.com/angular/angular.js/commit/2f4437b3a149eafb899f25933bd6c713b167d10e)

$animate.addClass, $animate.removeClass and $animate.setClass will no longer start the animation
right after being called in the directive code. The animation will only commence once a digest
has passed. This means that all animation-related testing code requires an extra digest to kick
off the animation.

```js
//before this fix
$animate.addClass(element, 'super');
expect(element).toHaveClass('super');

//now
$animate.addClass(element, 'super');
$rootScope.$digest();
expect(element).toHaveClass('super');
```

$animate will also tally the amount of times classes are added and removed and only animate
the left over classes once the digest kicks in. This means that for any directive code that
adds and removes the same CSS class on the same element then this may result in no animation
being triggered at all.

```js
$animate.addClass(element, 'klass');
$animate.removeClass(element, 'klass');

$rootScope.$digest();

//nothing happens...
```


- **$compile/ngBind:** due to [3660fd09](https://github.com/angular/angular.js/commit/3660fd0912d3ccf6def8c9f02d8d4c0621c8d91f),

The value of `$binding` data property on an element is always an array now
and the expressions do not include the curly braces `{{ ... }}`.


- **currencyFilter:** due to [c2aaddbe](https://github.com/angular/angular.js/commit/c2aaddbe4b21348aab8c13a78cdd6aaee846ae4e),
  previously the currency filter would convert null and undefined values into empty string, after this change
these values will be passed through.

Only cases when the currency filter is chained with another filter that doesn't expect null/undefined will be affected. This
should be very rare.

This change will not change the visual output of the filter because the interpolation will convert the null/undefined to
an empty string.

Closes #8605


- **numberFilter:** due to [2ae10f67](https://github.com/angular/angular.js/commit/2ae10f67fcde3e172f695956301ef796b68a50c2),
  previously the number filter would convert null and undefined values into empty string, after this change
these values will be passed through.

Only cases when the number filter is chained with another filter that doesn't expect null/undefined will be affected. This
should be very rare.

This change will not change the visual output of the filter because the interpolation will convert the null/undefined to
an empty string.

Closes #8605
Closes #8842


- **input:**
  - due to [77ce5b89](https://github.com/angular/angular.js/commit/77ce5b89f97aa83c3eb1fe2e19375ef00a822015),

NgModel.viewValue will always be used when rendering validations for `minlength` and `maxlength`.

Closes #7967
Closes #8811

- **input:**
  - due to [29f0b568](https://github.com/angular/angular.js/commit/29f0b568debab7810752969d363d337099e96cdc),


According to the HTML5 spec `input[time]` should create dates
based on the year 1970 (used to be based on the year 1900).

Related to #8447.


- **ngModel**: due to [db044c40](https://github.com/angular/angular.js/commit/db044c408a7f8082758b96ab739348810c36e15a)

Any parser code from before that returned an `undefined` value
(or nothing at all) will now cause a parser failure. When this occurs
none of the validators present in `$validators` will run until the parser
error is gone. The error will be stored on `ngModel.$error`.




- **ngEventDirs:** due to [719c747c](https://github.com/angular/angular.js/commit/719c747cd892ee933e7e414a7dc97e657b88317d),

The `blur` and `focus` event fire synchronously, also during DOM operations
that remove elements. This lead to errors as the Angular model was not
in a consistent state. See this [fiddle](http://jsfiddle.net/fq1dq5yb/) for a demo.

This change executes the expression of those events using
`scope.$evalAsync` if an `$apply` is in progress, otherwise
keeps the old behavior.

Fixes #4979
Fixes #5945
Closes #8803
Closes #6910
Closes #5402

- **$compile:** due to [5f3f25a1](https://github.com/angular/angular.js/commit/5f3f25a1a6f9d4f2a66e2700df3b9c5606f1c255),

The returned value from directive controller constructors are now ignored, and only the constructed
instance itself will be attached to the node's expando. This change is necessary in order to ensure
that it's possible to bind properties to the controller's instance before the actual constructor is
invoked, as a convenience to developers.

In the past, the following would have worked:

```js
angular.module("myApp", []).
    directive("myDirective", function() {
        return {
            controller: function($scope) {
                return {
                    doAThing: function() { $scope.thingDone = true; },
                    undoAThing: function() { $scope.thingDone = false; }
                };
            },
            link: function(scope, element, attrs, ctrl) {
                ctrl.doAThing();
            }
        };
    });
```

However now, the reference to `doAThing()` will be undefined, because the return value of the controller's constructor is ignored. In order to work around this, one can opt for several strategies, including the use of `_.extend()` or `merge()` like routines, like so:

```js
angular.module("myApp", []).
    directive("myDirective", function() {
        return {
            controller: function($scope) {
                _.extend(this, {
                    doAThing: function() { $scope.thingDone = true; },
                    undoAThing: function() { $scope.thingDone = false; }
                });
            },
            link: function(scope, element, attrs, ctrl) {
                ctrl.doAThing();
            }
        };
    });
```



<a name="1.3.0-beta.19"></a>
# 1.3.0-beta.19 rafter-ascension (2014-08-22)


## Bug Fixes

- **$compile:**
  - use the correct namespace for transcluded SVG elements
  ([ffbd276d](https://github.com/angular/angular.js/commit/ffbd276d6def6ff35bfdb30553346e985f4a0de6),
   [#8716](https://github.com/angular/angular.js/issues/8716))
  - update the jQuery `.context` when an element is replaced by `replace:true` directive
  ([f02f7d9c](https://github.com/angular/angular.js/commit/f02f7d9c15deea9c5d83212301e2a5e18223bbe5),
   [#8253](https://github.com/angular/angular.js/issues/8253), [#7900](https://github.com/angular/angular.js/issues/7900))
- **$location:**
  - rewrite relative URI correctly if `path==='/'` in legacy html5Mode
  ([d18b2819](https://github.com/angular/angular.js/commit/d18b2819768e467897dee7bc223876ca23ea71b1),
   [#8684](https://github.com/angular/angular.js/issues/8684))
  - don't call `indexOf()` of undefined `href` attribute
  ([5b77e30c](https://github.com/angular/angular.js/commit/5b77e30c1ac49be7b079b82527a5631f68bac904),
   [#7721](https://github.com/angular/angular.js/issues/7721), [#8681](https://github.com/angular/angular.js/issues/8681))
- **$parse:** remove unused variable declaration in generated getters
  ([6acea115](https://github.com/angular/angular.js/commit/6acea1152f72a4026583897c67bea2839bc9e89e))
- **$sanitize:** sanitize javascript urls with comments
  ([b7e82a33](https://github.com/angular/angular.js/commit/b7e82a33eee03fc683f982c6ee13d15d88b07f67),
   [#8274](https://github.com/angular/angular.js/issues/8274))
- **$watchGroup:** call listener once when the `watchExpressions` array is empty
  ([bf0e8373](https://github.com/angular/angular.js/commit/bf0e83732aa02c7aa08d0ccdf122116235fcfa11))
- **Angular:** make Date comparison in `equals()` `NaN`-aware
  ([693e846a](https://github.com/angular/angular.js/commit/693e846add5089d0e516604ae4a109e445fd3664),
   [#8650](https://github.com/angular/angular.js/issues/8650), [#8715](https://github.com/angular/angular.js/issues/8715))
- **Scope:** don't clear the phase when an exception is thrown from asyncQueue or watch
  ([bf1a57ad](https://github.com/angular/angular.js/commit/bf1a57ad4822bb152fdd4d2fb54c0689e466481b))
- **copy:** clear array destinations correctly for non-array sources
  ([a603e202](https://github.com/angular/angular.js/commit/a603e202cc7e048c2ab6f12dee1cc8f277cf6f4f),
   [#8610](https://github.com/angular/angular.js/issues/8610), [#8702](https://github.com/angular/angular.js/issues/8702))
- **forEach:** match behaviour of Array.prototype.forEach (ignore missing properties)
  ([36230194](https://github.com/angular/angular.js/commit/36230194be8aa417b0af33d618060829a75c4c5f),
   [#8510](https://github.com/angular/angular.js/issues/8510), [#8522](https://github.com/angular/angular.js/issues/8522), [#8525](https://github.com/angular/angular.js/issues/8525))
- **input:**
  - use lowercase method to account for undefined type
  ([066c0499](https://github.com/angular/angular.js/commit/066c049957a8af2fe449040eca2f1cb499655e32))
  - by default, do not trim input[type=password] values
  ([a7fb357f](https://github.com/angular/angular.js/commit/a7fb357fa122e0a056ce1de838a2dfaf1ebc2953),
   [#8250](https://github.com/angular/angular.js/issues/8250), [#8230](https://github.com/angular/angular.js/issues/8230))
- **jQuery:** cooperate with other libraries monkey-patching jQuery.cleanData
  ([b9389b26](https://github.com/angular/angular.js/commit/b9389b26ba2cf6aa70372fa32a7b28c62d174bf5),
   [#8471](https://github.com/angular/angular.js/issues/8471))
- **jqLite:**
  - clone wrapNode in jqlite/wrap
  ([77d3e754](https://github.com/angular/angular.js/commit/77d3e7544642396d868aa49b85f0c027e8057bd7),
   [#3860](https://github.com/angular/angular.js/issues/3860), [#4194](https://github.com/angular/angular.js/issues/4194))
  - revert the `ready()` optimization until jQuery does the same
  ([1bdca93d](https://github.com/angular/angular.js/commit/1bdca93d708ce9441b26d00e564210755395edf7))
- **linky:** handle quotes around email addresses
  ([a9d22712](https://github.com/angular/angular.js/commit/a9d227120dc2d433372da415a450e56b783b57a0),
   [#8520](https://github.com/angular/angular.js/issues/8520))
- **minErr:** encode btstrpd error input to strip angle brackets
  ([0872388a](https://github.com/angular/angular.js/commit/0872388a1b88b8637fdb0fb1ebbee269bead0508),
   [#8683](https://github.com/angular/angular.js/issues/8683))
- **ngRepeat:**
  - allow aliasAs identifiers which contain but do not match reserved words
  ([d713ad1b](https://github.com/angular/angular.js/commit/d713ad1b6607389649fbb8d12ac103565b02a1d4),
   [#8729](https://github.com/angular/angular.js/issues/8729))
  - make allowed aliasAs expressions more strict
  ([09b29870](https://github.com/angular/angular.js/commit/09b298705f74255aff55bb7e4ba200c4200d712d),
   [#8438](https://github.com/angular/angular.js/issues/8438), [#8440](https://github.com/angular/angular.js/issues/8440))


## Features

- **$compile:**
  - use allOrNothing interpolation for ngAttr*
  ([09de7b5d](https://github.com/angular/angular.js/commit/09de7b5db466498becb295ecf5c1d0a698b1512c),
   [#8376](https://github.com/angular/angular.js/issues/8376), [#8399](https://github.com/angular/angular.js/issues/8399))
- **benchpress:** configure benchpress grunt task
  ([6bdaa4bc](https://github.com/angular/angular.js/commit/6bdaa4bc213805a58f51e9f5285dfe03bb06ddc3))
- **jqLite:** implement the `detach` method
  ([1a05daf5](https://github.com/angular/angular.js/commit/1a05daf5dc67813528afdb88086766dc22b6c0df),
   [#5461](https://github.com/angular/angular.js/issues/5461))
- **ngRoute:** add method for changing url params
  ([77a1acc7](https://github.com/angular/angular.js/commit/77a1acc7fcad7a8a7d0376b33d38a8977372cfe2))


## Performance Improvements

- **$compile:**
  - don't register $destroy callbacks on element-transcluded nodes
  ([b5f7970b](https://github.com/angular/angular.js/commit/b5f7970be5950580bde4de0002a578daf3ae3aac))
  - refactor publicLinkFn to simplify the code and use 'for in' loop
  ([645625cf](https://github.com/angular/angular.js/commit/645625cf349a4be57691a7bf418b2386b4c1a53d))
  - clone the nodeList during linking only if necessary
  ([3e0a2e1f](https://github.com/angular/angular.js/commit/3e0a2e1f3367a5b4ae7d8de6cff559f522aacfba))
  - delay object initialization in nodeLinkFn
  ([31ed0af7](https://github.com/angular/angular.js/commit/31ed0af74b0081906415dcefe5610e1217cc0c48))
  - optimize nodeLinkFn
  ([35134a0e](https://github.com/angular/angular.js/commit/35134a0e237d193cd7d3995dacfdc6bf3e92635e))
  - optimize publicLinkFn
  ([274e9c4d](https://github.com/angular/angular.js/commit/274e9c4ddfd64138d39fcf84047aabc3ccde2f0b))
- **$interpolate:** do not keep empty separators
  ([94b5c9f0](https://github.com/angular/angular.js/commit/94b5c9f00edff7fa631d09316ceb9c7fd4c6426a))
- **$parse:**
  - don't bind filters to a context
  ([8863b9d0](https://github.com/angular/angular.js/commit/8863b9d04c722b278fa93c5d66ad1e578ad6eb1f))
  - optimize filter implementation
  ([ece6ef47](https://github.com/angular/angular.js/commit/ece6ef479c741f17fc217d743cad64c516dbed27))
  - speed up fn invocation for no args case
  ([a17578ad](https://github.com/angular/angular.js/commit/a17578ad3db5d1375aec1d601055ab718eeafd10))
  - speed up fn invocation by optimizing arg collection
  ([fecfc5b0](https://github.com/angular/angular.js/commit/fecfc5b09feb7e4079364013b0beb6bf204ade2a))
  - use no-proto maps as caches and avoid hasOwnProperty checks
  ([d302ea0c](https://github.com/angular/angular.js/commit/d302ea0cfade2787d7cc500398b7dcd3e4eff945))
  - trim expression only if string
  ([a1341223](https://github.com/angular/angular.js/commit/a1341223c084c8188671bb8d6ea1608490b66f9f))
- **$rootScope:** do not use `Function::call` when not needed
  ([7eae29e5](https://github.com/angular/angular.js/commit/7eae29e5ab478ccb7e02fee8311f8b99ea1d165d))
- **Scope:**
  - optimize `$watchCollection` when used for watching objects
  ([e822e906](https://github.com/angular/angular.js/commit/e822e9061c2a605649d91abbd641f757e2829275))
  - don't use forEach in
  ([301463a2](https://github.com/angular/angular.js/commit/301463a2e249011d7cb696c6cf34254f8317a706))
  - watchCollection optimization
  ([7d96ab0d](https://github.com/angular/angular.js/commit/7d96ab0d132d923ec3e3a212aaf9d79f1d4a02de))
  - exit $broadcast early if nobody is listening for the given event
  ([a09fa356](https://github.com/angular/angular.js/commit/a09fa356416c033a52666f3becf00524ecff3a03))
  - use remove the need for the extra watch in $watchGroup
  ([3f0e642e](https://github.com/angular/angular.js/commit/3f0e642eefcbbb315839c4456ba6ac029a7b8a20),
   [#8396](https://github.com/angular/angular.js/issues/8396))
- **benchpress:** add benchpress node module and port over large table test
  ([1229334f](https://github.com/angular/angular.js/commit/1229334fbd8c778e95785d6a5e5589099ce655f7))
- **isObject:** use strict comparison
  ([d208ba25](https://github.com/angular/angular.js/commit/d208ba254442649d35f96c76bcd9e47326ec59f3))
- **jqLite:**
  - simplify jqLiteDealoc
  ([f8f7a1df](https://github.com/angular/angular.js/commit/f8f7a1df34560222cb5d2e18d4be996f5553815a))
  - optimize event handler
  ([d05f27e2](https://github.com/angular/angular.js/commit/d05f27e274c41c33eebf4fe8035715d3f6596069))
  - only take `str.split()` path when needed
  ([187b1b8e](https://github.com/angular/angular.js/commit/187b1b8ef45babd86afa853dc9321cd23160096e),
   [#8648](https://github.com/angular/angular.js/issues/8648))
  - optimize `off()`
  ([abb17cce](https://github.com/angular/angular.js/commit/abb17cce8b459e4646d1c2a2428b691c3d95fb4c))
  - refactor jqLiteExpandoStore to minimize access to expensive element.ng339 expando property
  ([1e8698b3](https://github.com/angular/angular.js/commit/1e8698b33e61b1a196f05f42856a2da4590a10e1))
  - microoptimization in chaining fn
  ([fafbd494](https://github.com/angular/angular.js/commit/fafbd494907a8c068d79415b7ba8f42f283be521))
  - don't use String#split in on() unless we need it
  ([bda673f8](https://github.com/angular/angular.js/commit/bda673f8e785f299407c8c45887f37448a0f0192))
  - don't check isString many times in constructor
  ([443b521e](https://github.com/angular/angular.js/commit/443b521e22f9ec7009b913a2fe78caee0a515e87))
  - optimize jqLiteAcceptsData method
  ([b493c62f](https://github.com/angular/angular.js/commit/b493c62f6b3e4288f5dee7c8b5952e088c2e3329))
  - optimize `append()` and `after()`
  ([8d933bf9](https://github.com/angular/angular.js/commit/8d933bf99520fe3936e33d3ee28fd37e574b99de))
  - don't register DOM listener for $destroy event
  ([6251751a](https://github.com/angular/angular.js/commit/6251751ad7bc2f3621db538edb5a9d7313a4ce6d))
  - optimize event listener registration
  ([566f1015](https://github.com/angular/angular.js/commit/566f1015d27118d259e0886910d6b73b3cb0eb10))
  - improve createEventHandler method by switching from forEach to for loop
  ([e9cd6dc0](https://github.com/angular/angular.js/commit/e9cd6dc055cb7bd80ae9232d8985b2bc3999135e))
  - don't use `forEach` in `off()`
  ([960a8410](https://github.com/angular/angular.js/commit/960a8410515b2d7d461d7c95e8a2ca3d75129087))
  - don't recreate the Node.contains polyfill
  ([d1536e7c](https://github.com/angular/angular.js/commit/d1536e7c8bf60549096138d08953a43190c7b1a6))
  - speed up shallowCopy and special case Attributes cloning
  ([54fa16e4](https://github.com/angular/angular.js/commit/54fa16e45d8769ce6708a28388326db0eea53c7e))
- **ngBind:** bypass jquery/jqlite when setting text
  ([0a738ce1](https://github.com/angular/angular.js/commit/0a738ce1760f38efe45e79aa133442be09b56803))
- **ngRepeat:**
  - simplify code and remove duplicate array.length access
  ([08eb0558](https://github.com/angular/angular.js/commit/08eb05583bf39c63fef43b4faf29c61360699c81))
  - optimize marking of nodes that are being removed via an animation
  ([36e35b2c](https://github.com/angular/angular.js/commit/36e35b2cb17c5ff7c43746d9ac0a259f77ff494e))
  - use no-proto objects for blockMaps
  ([13d113c5](https://github.com/angular/angular.js/commit/13d113c522f124b91a1fd8606c22bbd399abf121))
  - move work to compile fn
  ([bdd853cb](https://github.com/angular/angular.js/commit/bdd853cb83839eef9901af164293611eaa23ee2c))
  - move updateScope fn to factory and reuse it for all repeaters
  ([e58d65a5](https://github.com/angular/angular.js/commit/e58d65a520cfbc630cbfbc248479416777ca16b2))
  - clone boundary comment nodes
  ([fbd48845](https://github.com/angular/angular.js/commit/fbd48845e0e88e9935f82fe4c9f686ad78b5d924))


## Breaking Changes

- **$compile:**
  - due to [09de7b5d](https://github.com/angular/angular.js/commit/09de7b5db466498becb295ecf5c1d0a698b1512c),


Now, `ng-attr-*` will never add the attribute to the DOM if any of the interpolated expressions
evaluate to `undefined`.

To work around this, initialize values which are intended to be the empty string with the
empty string:

For example, given the following markup:

```html
<div ng-attr-style="border-radius: {{value}}{{units}}"></div>
```

If `$scope.value` is `4`, and `$scope.units` is `undefined`, the resulting markup is unchanged:

```html
<div ng-attr-style="border-radius: {{value}}{{units}}"></div>
```

However, if $scope.units is `""`, then the resulting markup is updated:

```html
<div ng-attr-style="border-radius: {{value}}{{units}}" style="border-radius: 4"></div>
```

Closes #8376
Closes #8399

  - due to [0d608d04](https://github.com/angular/angular.js/commit/0d608d041f37a659d8d8ba7a9b688e132587035d),
  element-transcluded directives now have an extra comment automatically appended to their cloned DOM

This comment is usually needed to keep track the end boundary in the event child directives modify the root node(s).
If not used for this purpose it can be safely ignored.

  - due to [75c4cbf8](https://github.com/angular/angular.js/commit/75c4cbf81fcd6d49656d3cb044e59e5fd24e0479),
  `directive.type` was renamed to `directive.templateNamespace`

This change is breaking only within 1.3.0-beta releases: `directive.type` was renamed to `directive.templateNamespace`

The property name `type` was too general.

- **$parse:** due to [8863b9d0](https://github.com/angular/angular.js/commit/8863b9d04c722b278fa93c5d66ad1e578ad6eb1f),
   `this` in filters is now undefined and no longer the scope

It's a bad practice for filters to have hidden dependencies, so pulling stuff from scope directly
is not a good idea. Scope being the filter context was never documented as public API, so we don't
expect that any significant code depends on this behavior.

If an existing filter has a dependency on the scope instance, the scope reference can
be passed into the filter as a filter argument (this is highly discouraged for new code):

Before: `{{ user.name | customFilter }}`
After: `{{ user.name | customFilter:this }}`

- **Scope:** due to [0554c1aa](https://github.com/angular/angular.js/commit/0554c1aae49a81691154a77e70b602b0f24dca81),
  `deregisterNotifier` callback for `$watch` is no longer available

This API was available only in the last few 1.3 beta versions and is not
very useful for applications, so we don't expect that anyone will be affected
by this change.

- **input:** due to [a7fb357f](https://github.com/angular/angular.js/commit/a7fb357fa122e0a056ce1de838a2dfaf1ebc2953),
  by default, do not trim `input[type=password]` values.

Previously, `input[type=password]` would trim values by default, and would require an explicit `ng-trim="false"`
to disable the trimming behaviour. After this change, `ng-trim` no longer affects `input[type=password]`, and will
never trim the password value.

Closes #8250
Closes #8230



<a name="1.3.0-beta.18"></a>
# 1.3.0-beta.18 spontaneous-combustion (2014-08-12)


## Bug Fixes

- **$compile:** make '='-bindings NaN-aware
  ([5038bf79](https://github.com/angular/angular.js/commit/5038bf79c6c8251d7449d887b44a4321e619c534),
   [#8553](https://github.com/angular/angular.js/issues/8553), [#8554](https://github.com/angular/angular.js/issues/8554))
- **$location:** add semicolon to whitelist of delimiters to unencode
  ([36258033](https://github.com/angular/angular.js/commit/3625803349de04f175f87a22cbb608738003811a),
   [#5019](https://github.com/angular/angular.js/issues/5019))
- **$parse:**
  - one-time binding for literal expressions works as expected
  ([c024f282](https://github.com/angular/angular.js/commit/c024f28217cf8eedd695dd4b933ecf2ba4243c15),
   [#8209](https://github.com/angular/angular.js/issues/8209))
  - correctly assign expressions who's path is undefined and that use brackets notation
  ([c03ad249](https://github.com/angular/angular.js/commit/c03ad249033e701f3ad7aa358102e1cb87f5025c),
   [#8039](https://github.com/angular/angular.js/issues/8039))
- **Scope:** add deregisterNotifier to oneTimeLiteralWatch signature
  ([a001a417](https://github.com/angular/angular.js/commit/a001a417d5c12bad0fa09c88e045622b95239e2f))
- **jqLite:**
  - allow `triggerHandler()` to accept custom event
  ([01d81cda](https://github.com/angular/angular.js/commit/01d81cdab3dbbcb8b4204769eb5272096eb0837f),
   [#8469](https://github.com/angular/angular.js/issues/8469))
  - fix regression where mutating the dom tree on a event breaks jqLite.remove
  ([a00c9bca](https://github.com/angular/angular.js/commit/a00c9bca401abe5b5b0a217be82333056422c811),
   [#8359](https://github.com/angular/angular.js/issues/8359))
- **ngSanitize:** ensure `html` is a string in htmlParser()
  ([34781f18](https://github.com/angular/angular.js/commit/34781f18cb75ded9ae29f4b78f5bacd079f76709),
   [#8417](https://github.com/angular/angular.js/issues/8417), [#8416](https://github.com/angular/angular.js/issues/8416))
- **select:**
  - ensure that at least one option has the `selected` attribute set
  ([25a476ea](https://github.com/angular/angular.js/commit/25a476ea096b200fb4f422aaa9cd7215e2596ad3),
   [#8366](https://github.com/angular/angular.js/issues/8366), [#8429](https://github.com/angular/angular.js/issues/8429))
  - do not update selected property of an option element on digest with no change event
  ([cdc7db3f](https://github.com/angular/angular.js/commit/cdc7db3f35368a9175ed96c63f4bf56593fe1876),
   [#8221](https://github.com/angular/angular.js/issues/8221), [#7715](https://github.com/angular/angular.js/issues/7715))


## Features

- **$parse:** allow for assignments in ternary operator branches
  ([2d678f1d](https://github.com/angular/angular.js/commit/2d678f1d0a3714fdd49e582b92787312af129947),
   [#8512](https://github.com/angular/angular.js/issues/8512), [#8484](https://github.com/angular/angular.js/issues/8484))
- **form:** Add new $submitted state to forms
  ([108a69be](https://github.com/angular/angular.js/commit/108a69be17df5884d026c57b2be3235c576250fe),
   [#8056](https://github.com/angular/angular.js/issues/8056))
- **http:** allow caching for JSONP requests
  ([3607c982](https://github.com/angular/angular.js/commit/3607c9822f57b4d01b3f09a6ae4efc7168bec6c5),
   [#1947](https://github.com/angular/angular.js/issues/1947), [#8356](https://github.com/angular/angular.js/issues/8356))
- **jQuery:** upgrade to jQuery to 2.1.1
  ([9e7cb3c3](https://github.com/angular/angular.js/commit/9e7cb3c37543008e6236bb5a2c4536df2e1e43a9))
- **ngMock:** allow override of when/expect definitions
  ([477626d8](https://github.com/angular/angular.js/commit/477626d846b4de65d1d5c7071e6a94361395ff42),
   [#5766](https://github.com/angular/angular.js/issues/5766), [#8352](https://github.com/angular/angular.js/issues/8352))


## Performance Improvements

- **$q:** move Deferred and Promise methods to prototypes
  ([23bc92b1](https://github.com/angular/angular.js/commit/23bc92b17df882a907fb326320f0622717fefe7b),
   [#8300](https://github.com/angular/angular.js/issues/8300))
- **input:** prevent additional $digest when input is already touched
  ([dd2a803f](https://github.com/angular/angular.js/commit/dd2a803f4f03ab629a51623c026d3e3f9dc9e91f),
   [#8450](https://github.com/angular/angular.js/issues/8450))


## Breaking Changes

- **jQuery:** due to [9e7cb3c3](https://github.com/angular/angular.js/commit/9e7cb3c37543008e6236bb5a2c4536df2e1e43a9),
  Angular no longer supports jQuery versions below 2.1.1.
- **$q:** due to [23bc92b1](https://github.com/angular/angular.js/commit/23bc92b17df882a907fb326320f0622717fefe7b),
  Promises methods are no longer enumerated when using for-loops with `hasOwnProperty` check. E.g. `angular.extends`

