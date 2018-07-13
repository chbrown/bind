## bind

[![latest version published to npm](https://badge.fury.io/js/@chbrown%2Fbind.svg)](https://www.npmjs.com/package/@chbrown/bind)

`@bind` decorator for TypeScript.

### Install

```shell
npm install -S @chbrown/bind
```

### Example

```ts
import bind from '@chbrown/bind'

class ClickCounter extends React.Component<{}, {clicks: number}> {
  state: {clicks: number} = {clicks: 0}
  @bind
  onClick(ev: React.FormEvent) {
    this.setState(({clicks}) => ({clicks: clicks + 1}))
  }
  render() {
    const {clicks} = this.state
    return (
      <div>
        <button onClick={this.onClick}>Click here</button>
        <p>Clicked {clicks} times</p>
      </div>
    )
  }
}
```


## License

Copyright 2018 Christopher Brown.
[MIT Licensed](https://chbrown.github.io/licenses/MIT/#2018).
