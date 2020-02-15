# 设备信息

## 安装

```shell script
eeui plugin install https://github.com/aipaw/eeui-plugin-deviceInfo
```

## 卸载

```shell script
eeui plugin uninstall https://github.com/aipaw/eeui-plugin-deviceInfo
```

## 引用

```js
const deviceInfo = app.requireModule("eeui/deviceInfo");
```

### info(callback) 获取信息

#### 参数

1.  [`callback`] (Function)

#### 返回

1.  `result` (Object)
    *   `model` (String)

    *   `vendor` (String)

    *   `uuid` (String)

    *   `platform` (String) (`Android` | `iOS`)

    *   `version` (String)

    *   `language` (String)

    *   `isVirtual` (Boolean) ( _iOS Only_ )

#### 示例

```
deviceInfo.info((ret) => {
    console.log(ret)
})
```

* * *

### netStatus(callback) 获取网络状态

#### 参数

1.  [`callback`] (Function)

#### 返回

1.  `result` (Object)
    *   `type` (String) (`wifi` | `3g` | `4g` | `2g` | `unkown`)

#### 示例

```
deviceInfo.netStatus((ret) => {
    console.log(ret)
})
```

* * *

### setVibrate(time) 振动

#### 参数

1.  [`time`] (Int) (ms, default: `500`) ( _Android Only_ )

#### 示例

```
deviceInfo.setVibrate()
```

```
deviceInfo.setVibrate(2000)
```

* * *

### screenInfo(callback) 获取屏幕信息

#### 参数

1.  [`callback`] (Function)

#### 返回

1.  `result` (Object)
    *   `height` (Int)

    *   `width` (Int)

    *   `scale` (Float)

    *   `dpiX` (Int)

    *   `dpiY` (Int)

#### 示例

```
deviceInfo.screenInfo((ret) => {
    console.log(ret)
})
```

* * *

### getBrightness(callback) 获取屏幕亮度

#### 参数

1.  [`callback`] (Function)

#### 返回

1.  `result` (Object)
    *   `brightness` (Float) (0~1)

#### 示例

```
deviceInfo.getBrightness((ret) => {
    console.log(ret)
})
```

* * *

### setBrightness(value, callback) 设置屏幕亮度

#### 参数

1.  `value` (Float) (0~1)

2.  [`callback`] (Function)

#### 返回

1.  `result` (Object)
    *   `brightness` (Float) (0~1)

#### 示例

```
deviceInfo.setBrightness(1)
```

```
deviceInfo.setBrightness(1, (ret) => {
    console.log(ret)
})
```

* * *

### getOrientation(callback) 获取屏幕方向状态

#### 参数

1.  [`callback`] (Function)

#### 返回

1.  `result` (Object)
    *   `orientation` (String) (`portrait` | `landscape` | `landscape-left` | `landscape-right` | `portrait-down`)

#### 示例

```
deviceInfo.getOrientation((ret) => {
    console.log(ret)
})
```

* * *

### getVolume(callback) 获取音量

#### 参数

1.  [`callback`] (Function)

#### 返回

1.  `result` (Object)
    *   `volume` (Float) (0~1)

#### 示例

```
deviceInfo.getVolume((ret) => {
    console.log(ret)
})
```

* * *

### setVolume(value, callback) 设置音量

#### 参数

1.  `value` (Float) (0~1)

2.  [`callback`] (Function)

#### 返回

1.  `result` (Object)
    *   `volume` (Float) (0~1)

#### 示例

```
deviceInfo.setVolume(1)
```

```
deviceInfo.setVolume(1, (ret) => {
    console.log(ret)
})
```

* * *

### batteryStatus(callback) 获取电池状态

#### 参数

1.  [`callback`] (Function)

#### 返回

1.  `result` (Object)
    *   `level` (Int) (0~100)

    *   `isPlugged` (Boolean)

#### 示例

```
deviceInfo.batteryStatus((ret) => {
    console.log(ret)
})
```
