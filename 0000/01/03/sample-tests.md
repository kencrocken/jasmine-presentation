## Test Anatomy

Tests are grouped together in a "test suite."
Test suites are started with the `describe` function.  

- Accepts a string and function.  
- The string is a descriptive statement.  
- The function holds the code for the suite.  

Within the `describe` function we define the "specs." 

--

The `it` function defines our specs.  And is structured like `describe`.

Within the function, we call `expect` and pass an "Actual."  
The `expect` is chained to a "matcher" - and passed the expectation. 

```js

describe( 'A sample test suite', function() {

    it( 'has a dummy spec to test 2 + 2', function() {

        var four = 2+2;
        expect( four ).toEqual( 4 );

    });

});
```

--

## Things you can do.

- Lots of included matchers
- Create custom matchers
- Nest tests to group related specs
- `beforeEach`, `afterEach`
- Spies!

---

## Spies

Are test double functions that Jasmine can track.  

--

- A spy can stub any function and tracks calls to it and all arguments. <!-- .element: class="fragment" -->  
- A spy only exists in the describe or it block in which it is defined, and will be removed after each spec. <!-- .element: class="fragment" -->
- Special matchers for interacting with spies. <!-- .element: class="fragment" -->
    - `toHaveBeenCalled` : return true if the spy was called 
    - `toHaveBeenCalledTimes` : will pass if the spy was called the specified number of times 
    - `toHaveBeenCalledWith` : will return true if the argument list matches any of the recorded calls to the spy 