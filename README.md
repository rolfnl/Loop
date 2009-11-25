Loop
====

A Utility Class. Its methods can be implemented with  [Class-implement][1] into any [Class][2]. Used to run a class method on a periodical.

Useful in galleries, slideshows, tickers, sprite animations, pulsing, logout scripts, etc.  Anything that needs to run the same function repeatedly.

### Example:

    var Widget = new Class({
  
      Implements: Loop,
  
      initialize: function(log){
        this.setLoop(this.update, 1000);
        this.log = document.id(log);
      },
  
      update: function(count){
        this.log.set('text',"Looped " + count + " times");
      }
  
    });
    
    var myWidget = new Widget('log').startLoop();