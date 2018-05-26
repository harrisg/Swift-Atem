# BMD Atem Protocol implementation

Implementation of BlackMagicDesign's ATEM communication protocol in Swift. It is written on top of Apple's new networking library [NIO](https://github.com/apple/swift-nio) and implements both sides of the protocol: the control panel and the switcher side. This means that you can not only use it to control atem switchers but also to connect to your control panels without the need for a switcher. Opening a whole new world of applications for the Atem control panels. An example can be found at [Atem-Simulator](https://github.com/Dev1an/Atem-Simulator)

## Usage

### Controller

```swift
try? Controller(ipAddress: "10.1.0.67") { handler in
	handler.when{ (change: PreviewBusChanged) in
		print(change) // prints: 'Preview bus changed to input(x)'
	}
}
```

### Switcher

Code example coming soon