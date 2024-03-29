 **Debounce**
 
###### realization for type scripts 

----
how to use :

```  const callBackWithArgs = (value: number) => value * 2;
  const fn = debounce(callBackWithArgs, 100, true)(2); // return 4
  
  const callBack = (msg: string) => console.log(msg);
  const fn = debounce(callBack, 1500);

  fn('a');
  fn('b');
  fn('c');
  // the output is 'c'
```  

## API

### debounce(fn, wait, [ immediate || false ])

  Creates and returns a new debounced version of the passed function that
  will postpone its execution until after wait milliseconds have elapsed
  since the last time it was invoked.

  Pass `true` for the `immediate` parameter to cause debounce to trigger
  the function on the leading edge instead of the trailing edge of the wait
  interval. Useful in circumstances like preventing accidental double-clicks
  on a "submit" button from firing a second time.

  The debounced function returned has a property 'clear' that is a 
  function that will clear any scheduled future executions of your function.

  The debounced function returned has a property 'flush' that is a 
  function that will immediately execute the function if and only if execution is scheduled,
  and reset the execution timer for subsequent invocations of the debounced
  function.

## License

  MIT

  Original implementation is from [`underscore.js`](http://underscorejs.org/)
  which also has an MIT license.
