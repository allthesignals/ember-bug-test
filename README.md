# Test-app

This repo illustrates this bug: https://github.com/emberjs/ember.js/issues/4570

Essentially, the #toggle function, which is called on a given (null/falsey) controller value input, at first sets the value to "true", sets the value to false on a second trigger, and finally sets the value to false on the third trigger. 

True -> False -> False -> True.

I can't figure out why Ember is doing this.
