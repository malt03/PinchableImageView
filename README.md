# PinchableImageView

[![Platform](https://img.shields.io/cocoapods/p/PinchableImageView.svg?style=flat)](http://cocoapods.org/pods/PinchableImageView)
![Language](https://img.shields.io/badge/language-Swift%203.0-orange.svg)
[![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat)](https://github.com/Carthage/Carthage)
[![CocoaPods](https://img.shields.io/cocoapods/v/PinchableImageView.svg?style=flat)](http://cocoapods.org/pods/PinchableImageView)
![License](https://img.shields.io/github/license/malt03/PinchableImageView.svg?style=flat)

![Screen Shot](https://raw.githubusercontent.com/malt03/PinchableImageView/master/Screenshot.gif)

## Usage

### Initialize
```swift
let imageView = PinchableImageView()
imageView.image = UIImage(named: "lena")!
imageView.sizeToFit()
imageView.center = view.center
view.addSubview(imageView)
```

### Initialize corner views for rotate
```swift
imageView.addCornerViews([.LeftTop: cornerView])
```

### Initialize corner views without rotate
```swift
imageView.addCornerViews([.LeftTop: cornerView], panEnabled: false)
```

### Delegate
```swift
protocol PinchableImageViewDelegate {
  optional func pinchableImageViewTouchesBegan(pinchableImageView: PinchableImageView, touches: Set<UITouch>, withEvent event: UIEvent?)
  optional func pinchableImageViewTouchesMoved(pinchableImageView: PinchableImageView, touches: Set<UITouch>, withEvent event: UIEvent?)
  optional func pinchableImageViewTouchesEnded(pinchableImageView: PinchableImageView, touches: Set<UITouch>, withEvent event: UIEvent?)
}
```

## Installation via Carthage

PinchableImageView is available through [Carthage](https://github.com/Carthage/Carthage). To install
it, simply add the following line to your Cartfile:

```ruby
github "malt03/PinchableImageView"
```

## Installation via CocoaPods

PinchableImageView is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod "PinchableImageView"
```

## Author

Koji Murata, malt.koji@gmail.com

## License

PinchableImageView is available under the MIT license. See the LICENSE file for more info.
