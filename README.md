# javascript-email-address-duplicate-filter
Quick and dirty email duplicate filtering based on array of email address strings.

```javascript
  var emailInArr = ['mike@gmail.com', 'bob@gmail.com', 'alice@gmail.com', 'mike@gmail.com', 'jelly@gmail.com', 'bob@gmail.com'];
  var emailOutArr = [emailInArr[0]];
  
  emailInArr.map(function(item){
    var isInArray = function(item) {
          var isTrue = false;
          for (var i = 0; i <= emailOutArr.length; ++i) {
            if (item === emailOutArr[i]) {
              isTrue = true;
            }
          }
          if(!isTrue) {
            emailOutArr.push(item);
          }
        };
    isInArray(item);
  });
  console.log(emailOutArr);
```
