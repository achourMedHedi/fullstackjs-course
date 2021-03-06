# State

* We can store a state of a component in `this.state` and for every change of this state, the component will be re-rendred.

* The state is initialized in the constructor then we can change it with the method `setState`.

## Example: Counter

```javascript
import React, { Component } from 'react'

class Counter extends Component{
  constructor(props){
      super(props)
      this.state = { // init state
        counter: 0
      }

      setInterval(() => {
        this.setState({ //change state
          counter: this.state.counter + 1
        })
      }, 1000)
  }

  render(){
    return(
      <div>
        <h1>Counter: {this.state.counter}</h1>
      </div>
    )
  }
}

export default Counter
```

## Exercise
Create a Countdown component which takes number of seconds as input (through props) and render a countdown to 0.
