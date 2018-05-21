---
UID: TP:xinput
ms.assetid: 5c8ac494-6872-3057-85f8-b67254b814c4
ms.author: windowsdriverdev
ms.date: 05/21/18
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: portal
---

# XInput Game Controller APIs



Overview of the XInput Game Controller APIs technology.

To develop XInput Game Controller APIs, you need these headers:

 * [xinput.h](..\xinput\index.md)

For the programming guide, see [XInput Game Controller APIs](https://review.docs.microsoft.com/en-us/win32-test/xinput).

## Functions

| Title   | Description   |
| ---- |:---- |
| [XInputEnable function](..\xinput\nf-xinput-xinputenable.md) | Sets the reporting state of XInput. |
| [XInputGetAudioDeviceIds function](..\xinput\nf-xinput-xinputgetaudiodeviceids.md) | Retrieves the sound rendering and sound capture audio device IDs that are associated with the headset connected to the specified controller. |
| [XInputGetBatteryInformation function](..\xinput\nf-xinput-xinputgetbatteryinformation.md) | Retrieves the battery type and charge status of a wireless controller. |
| [XInputGetCapabilities function](..\xinput\nf-xinput-xinputgetcapabilities.md) | Retrieves the capabilities and features of a connected controller. |
| [XInputGetDSoundAudioDeviceGuids function](..\xinput\nf-xinput-xinputgetdsoundaudiodeviceguids.md) | Gets the sound rendering and sound capture device GUIDs that are associated with the headset connected to the specified controller. |
| [XInputGetKeystroke function](..\xinput\nf-xinput-xinputgetkeystroke.md) | Retrieves a gamepad input event. |
| [XInputGetState function](..\xinput\nf-xinput-xinputgetstate.md) | Retrieves the current state of the specified controller. |
| [XInputSetState function](..\xinput\nf-xinput-xinputsetstate.md) | Sends data to a connected controller. This function is used to activate the vibration function of a controller. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [_XINPUT_BATTERY_INFORMATION structure](..\xinput\ns-xinput-_xinput_battery_information.md) | Contains information on battery type and charge state. |
| [_XINPUT_CAPABILITIES structure](..\xinput\ns-xinput-_xinput_capabilities.md) | Describes the capabilities of a connected controller. The XInputGetCapabilities function returns XINPUT_CAPABILITIES. |
| [_XINPUT_GAMEPAD structure](..\xinput\ns-xinput-_xinput_gamepad.md) | Describes the current state of the Xbox 360 Controller. |
| [_XINPUT_KEYSTROKE structure](..\xinput\ns-xinput-_xinput_keystroke.md) | Specifies keystroke data returned by XInputGetKeystroke. |
| [_XINPUT_STATE structure](..\xinput\ns-xinput-_xinput_state.md) | Represents the state of a controller. |
| [_XINPUT_VIBRATION structure](..\xinput\ns-xinput-_xinput_vibration.md) | Specifies motor speed levels for the vibration function of a controller. |
