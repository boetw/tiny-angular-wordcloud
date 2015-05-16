# tiny-angular-wordcloud
Tiny-angular-wordcloud is a simple wordcloud generator for AngularJS without any external dependencies 
consisting of a single directive.

### Version
0.0.1

### Installation
You can easily install tiny-angular-wordcloud with bower:

```sh
$ bower install tiny-angular-wordcloud --save
```

Once that is done you must add the the 'tangcloud' module to your Angular application:
```sh
angular.module('test', ['tangcloud'])
```

Now you can use the tangcloud directive in your html:
```sh
<tang-cloud></tangcloud>
```

### Supported variables
##### words - *required*
1. The name of a scope variable containing words in the format:
```sh
        $scope.words = [
            {word: "woord1", size: 1},
            {word: "woord2", size: 2},
            {word: "woord3", size: 3},
            {word: "woord4", size: 4},
        ];
```

2. An array of words in the format:
```sh
<tang-cloud words="[{word: 'woord1', size: 1},{word: 'woord2', size: 2}]"></tang-cloud>
```

##### width - *required*
the width of the wordcloud as a number of pixels. (in the future percentages will be supported)
```sh
<tang-cloud width="500"></tang-cloud>
```

##### height - *required*
the height of the wordcloud as a number of pixels. (in the future percentages will be supported)
```sh
<tang-cloud height="500"></tang-cloud>
```

### Styling
The size and styling of the different words is done using CSS based on the size of each word. You must implement these CSS classes yourself by using the following format:

```sh
.tangcloud-item-1 {
    font-size: 15px;
    color: green;
}
```

the 'size' number specified in the word objects determines the CSS class. So a word with size 6 will have the CSS class '.tangcloud-item-6'

a default CSS files with classes for size 1 - 10 can be found in the 'example' folder
License
----
GNU v2.0