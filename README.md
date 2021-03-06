# React Native QRCode (remobile)
A pure js show string as qrcode in react-native View.

## Installation
```sh
npm install @remobile/react-native-qrcode --save
```

## Usage

### Example
```js
'use strict';
var React = require('react');
var ReactNative = require('react-native');

var {
    StyleSheet,
    View,
    Text,
} = ReactNative;

var QRCode = require('@remobile/react-native-qrcode');

module.exports = React.createClass({
    componentDidMount() {
        setTimeout(()=>{
            this.setState({a:"方运江 is a good developer"});
        }, 2000)
    },
    getInitialState() {
        return {
            text: '42550564@qq.com'
        };
    },
    render() {
        return (
            <View style={styles.container}>
                <QRCode
                    text={this.state.text}
                    width={156}
                    height={156}
                    />
                <Text>
                    {this.state.text}
                </Text>
            </View>
        );
    }
});

var styles = StyleSheet.create({
    container: {
        flex: 1,
        alignItems: 'center',
        justifyContent: 'center'
    },
});
```

## Screencasts

![demo](https://github.com/remobile/react-native-qrcode/blob/master/screencasts/demo.gif)

#### Props
- `text: PropTypes.string.isRequired`
- `width: PropTypes.number [default:256]`
- `height: PropTypes.number [default:256]`
- `typeNumber: PropTypes.number [default:4]`
- `colorDark: PropTypes.string [default:"#000000"]`
- `colorLight: PropTypes.string [default:"#ffffff"]`
- `correctLevel: PropTypes.number [default:QRCode.QRErrorCorrectLevel.H] see index.js for detail`

### thanks
* this project come from https://github.com/davidshimjs/qrcodejs
