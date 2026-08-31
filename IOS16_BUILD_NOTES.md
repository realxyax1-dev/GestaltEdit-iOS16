# GestaltEdit iOS 16 build notes

This tree has been prepared for an iOS 16 SDK/Xcode 14-era build:

- Deployment target: iOS/iPadOS 16.0
- Swift language mode: 5.7
- Legacy Xcode project format (objectVersion 56)
- Modern icon-composer resource replaced by a classic `Assets.xcassets` AppIcon set
- iOS 27-only runtime version gate removed; runtime accepts iOS 16+
- MobileGestalt access now tries direct read/write first, then the optional bad_query bridge

This environment does not contain Xcode or the iOS 16 SDK, so the final device binary cannot be compiled here. The project itself is prepared to be built with Xcode 14.x + iOS 16 SDK.

Some MobileGestalt feature keys remain version-specific; compiling for iOS 16 does not make an iOS-26-only capability exist on iOS 16.
