# react-native-customisable-switch
A React Native module that allows you to customize switch (style, form and animation), available for android and IOS.

### Content
- [Installation](#installation)
- [Examples](#usage-example)
- [Properties](#component-properties)
- [Questions](#questions)

### Installation
```bash
npm install --save react-native-customisable-switch
```

### Examples
<p align="center">
    <img src="./examples.gif" />
</p>

```javascript
import React, { Component } from 'react';
import { Text, View } from 'react-native';
import Switch from 'react-native-customisable-switch';

export default class Test extends Component {
  constructor(props) {
    super(props);
    this.state = {
      switchOneValue: false,
      switchTwoValue: false,
      switchThreeValue: true,
    };
  }

  render() {
    const {
      switchOneValue,
      switchTwoValue,
      switchOneValue,
    } = this.state;

    return(
      <View style={styles.container}>
        <View style={styles.container}>
          <Switch
            value={switchOneValue}
            onChangeValue={() => this.setState({ switchOneValue: !switchOneValue })}
          />
        </View>
        <View style={styles.container}>
          <Switch
            value={switchTwoValue}
            onChangeValue={() => this.setState({ switchTwoValue: !switchTwoValue })}
            activeText={''}
            inactiveText={''}
            fontSize={16}
            activeTextColor={'rgba(255, 255, 255, 1)'}
            inactiveTextColor={'rgba(255, 255, 255, 1)'}
            activeBackgroundColor={'rgba(50, 163, 50, 1)'}
            inactiveBackgroundColor={'rgba(137, 137, 137, 1)'}
            activeButtonBackgroundColor={'rgba(255, 255, 255, 1)'}
            inactiveButtonBackgroundColor={'rgba(255, 255, 255, 1)'}
            switchWidth={70}
            switchHeight={30}
            switchBorderRadius={0}
            switchBorderColor={'rgba(0, 0, 0, 1)'}
            switchBorderWidth={0}
            buttonWidth={25}
            buttonHeight={25}
            buttonBorderRadius={0}
            buttonBorderColor={'rgba(0, 0, 0, 1)'}
            buttonBorderWidth={0}
            animationTime={150}
            padding={true}
          />
        </View>  
        <View style={styles.container}>
          <Switch
            value={switchThreeValue}
            onChangeValue={() => this.setState({ switchThreeValue: !switchThreeValue })}
            activeText={'On'}
            inactiveText={'Off'}
            fontSize={16}
            switchWidth={70}
            switchHeight={25}
            switchBorderRadius={12}
            switchBorderWidth={0}
            buttonWidth={25}
            buttonHeight={40}
            buttonBorderRadius={20}
            buttonBorderColor={'rgba(0, 0, 0, 1)'}
            buttonBorderWidth={0}
            animationTime={150}
            padding={true}
          />
        </View>
      </View>
    )
  }
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#464857',
    justifyContent: 'center',
    alignItems: 'center',
  },
)};
```

### Component Properties

| Property                | Type     | Default Value            | Description                                                               |
|-------------------------|----------|--------------------------|---------------------------------------------------------------------------|
| value                   | boolean  | false                    | Switch value to determine whether or not the switch is active or inactive |
| onChangeValue           | function | () => null               | Function to handle the change of the value property                       |
| activeText              | string   | "On"                     | Text when the switch is activate                                          |
| inactiveText            | string   | "Off"                    | Text when the switch is inactive                                          |
| fontSize                | number   | 16                       | Text Size for `activeText` and `inactiveText`                             |
| activeTextColor         | string   | "rgba(255, 255, 255, 1)" | Text color of `activeText`                                                |
| inactiveTextColor       | string   | "rgba(255, 255, 255, 1)" | Text color of `inactiveText`                                              |
| activeBackgroundColor   | string   | "rgba(50, 163, 50, 1)"   | Background color of the switch while active                               |
| inactiveBackgroundColor | string   | "rgba(137, 137, 137, 1)" | Background color of the switch while inactive                             |
| switchWidth             | number   | 70                       | Width of the switch                                                       |
| switchHeight            | number   | 30                       | Height of the switch                                                      |
| switchBorderRadius      | number   | 15                       | Border radius of the switch                                               |
| switchBorderColor       | string   | "rgba(0, 0, 0, 1)"       | Border color of the switch                                                |
| switchBorderWidth       | number   | 0                        | Border width of the switch                                                |
| buttonWidth             | number   | 25                       | Width of the button in the switch                                         |
| buttonHeight            | number   | 25                       | Height of the button in the switch                                        |
| buttonBorderRadius      | number   | 15                       | Border radius of the button in the switch                                 |
| buttonBorderColor       | string   | "rgba(0, 0, 0, 1)"       | Border color of the button in the switch                                  |
| buttonBorderWidth       | number   | 0                        | Border width of the button in the switch                                  |
| animationTime           | number   | 150                      | Time of toggle animation in milliseconds                                  |
| padding                 | boolean  | true                     | Whether the switch has a horizontal padding of 5 or not                   |


### Questions
Create an issue (https://github.com/baderahmed/react-native-customisable-switch/issues)
