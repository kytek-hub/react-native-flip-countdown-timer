# react-native-flip-countdown-timer [![Build Status](https://travis-ci.com/pritishvaidya/react-native-flip-countdown-timer.svg?token=Ekd1xJ5F1RtW2pbZwqK2&branch=master)](https://travis-ci.com/pritishvaidya/react-native-flip-countdown-timer) [![CodeFactor](https://www.codefactor.io/repository/github/pritishvaidya/react-native-flip-countdown-timer/badge)](https://www.codefactor.io/repository/github/pritishvaidya/react-native-flip-countdown-timer) [![Maintainability](https://api.codeclimate.com/v1/badges/9a237b9a845968a7a6be/maintainability)](https://codeclimate.com/github/pritishvaidya/react-native-flip-countdown-timer/maintainability) [![Test Coverage](https://api.codeclimate.com/v1/badges/9a237b9a845968a7a6be/test_coverage)](https://codeclimate.com/github/pritishvaidya/react-native-flip-countdown-timer/test_coverage) [![npm version](https://badge.fury.io/js/react-native-flip-countdown-timer.svg)](https://badge.fury.io/js/react-native-flip-countdown-timer) [![npm downloads](https://img.shields.io/npm/dt/react-native-flip-countdown-timer.svg)](https://npm-stat.com/charts.html?package=react-native-flip-countdown-timer&from=2018-02-17&to=2018-12-28) <a href="https://github.com/pritishvaidya/react-native-flip-countdown-timer/blob/master/README.md"><img src="https://img.shields.io/badge/module%20formats-umd%2C%20cjs%2C%20esm-green.svg" alt="module formats: umd, cjs, esm"></a>
> A Flip timer implementation in React Native

For a Normal Timer application you can checkout [react-native-flip-timer](https://github.com/pritishvaidya/react-native-flip-timer) repository.

## Show Cases
IOS            |  Android
:-------------------------:|:-------------------------:
![IOS](https://media.giphy.com/media/87halfgvRA0rEE6OfQ/giphy.gif)  |  ![Android](https://media.giphy.com/media/3XAbjm59akWOWj88bu/giphy.gif)

## Getting Started

- [Installation](#installation)
- [Basic Usage](#basic-usage)
- [Properties](#properties)
- [Defaults](#defaults)
- [Contribution](#contribution)
- [Questions](#questions)

### Installation

```bash
$ npm i react-native-flip-countdown-timer --save
```

### Basic Usage
```
import React, { Component } from 'react';
import {
  StyleSheet, View, TouchableOpacity, Text,
} from 'react-native';
import { CountdownTimer, FlipNumber } from 'react-native-flip-countdown-timer';

export default class App extends Component {
  state = {
    play: true,
  }

  play = () => {
    this.setState(({ play }) => ({ play: !play }));
  }

  render() {
    const { play } = this.state;
    return (
      <View style={styles.container}>
        <CountdownTimer time={500} play={play} />
        <TouchableOpacity style={styles.button} onPress={this.play}>
          <Text style={styles.text}>{play ? 'Pause' : 'Play'}</Text>
        </TouchableOpacity>
      </View>
    );
  }
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: 'white',
    alignItems: 'center',
    justifyContent: 'center',
  },
  button: {
    height: 40,
    backgroundColor: '#333333',
    width: 120,
    alignItems: 'center',
    justifyContent: 'center',
  },
  text: {
    fontSize: 16,
    fontWeight: 'bold',
    color: '#cccccc',
  },
});
```

### Properties
#### CountdownTimer Props
| Prop  | Default  | Type | Description |
| :------------ |---------------:| :---------------| :-----|
| time | required | `string / number` | Time (in seconds) |
| play | true | bool | Play the timer |
| wrapperStyle | `{}` | object | Wrapper for the CountdownTimer |
| flipNumberProps | [`{...}`](#flip-number-props) | `defaults` | Flip Number Props |

#### Flip Number Props
| Prop  | Default  | Type | Description |
| :------------ |---------------:| :---------------| :-----|
| number | required | `string / number` | Number Input |
| unit | `seconds` | `hours / minutes / seconds` | Number Input Unit |
| size | `number` | `deviceWidth / 6` | Size of the card |
| perspective | `250` | number | Perspective |
| numberWrapperStyle | `{}` | object | Wrapper Style |
| cardStyle | `{}` | object | Card Style |
| flipCardStyle | `{}` | object | Flip Card Style |
| numberStyle | `{}` | object | Number Style |

## Todos
- Full Coverage Tests for the Components
- Support for Labels

## Contribution

- [@pritishvaidya](mailto:pritishvaidya94@gmail.com) The main author.

## Questions

Feel free to [contact me](mailto:pritishvaidya94@gmail.com) or [create an issue](https://github.com/pritishvaidya/react-native-flip-countdown-timer/issues/new)

