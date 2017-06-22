## purpose
  test npm package DIY.
  
## step by step
1. **create description file of npm package.**

   You can use npm init to create the package.json. 
It will prompt you for values for the package.json fields. 
The two required fields are name and version. like this:
   > mkdir mypkg; cd mypkg; npm init
   
2. **edit main js file 'index.js'**
   ```js
   exports.test = function() {
    console.log("This is a message from the mypkg package");
   }
   ```

3. **edit test script (optional)**
   ```js
   console.log('execute test script.')
   ```
   
   and then, you can make test: as follow:
   > npm test

that's all about DIY your own npm moudule. :)

## usage
1. Make a new directory outside of your project and cd into it,
   edit package.json , add dependency of your own package:
   > cd ../; mkdir mytest; cd mytest;
   
   and then, edit package.json like this:
  ```js
     "name": "my_test",
     "dependencies": {
       "mypkg": "file:../mypkg"
     } 
   }
  ```
2. execute:
   > npm install
   
   you can see output as follow:
   ```js
    my_test@ /Users/changxun/Code/testdir
    └── mypkg@1.0.0 

    npm WARN xun_test@ No description
    npm WARN xun_test@ No repository field.
    npm WARN xun_test@ No license field.
    ```
      
