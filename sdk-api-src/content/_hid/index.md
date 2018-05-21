---
UID: TP:hid
ms.assetid: 87c002be-da96-313a-bae1-c6a49c9ce065
ms.author: windowsdriverdev
ms.date: 05/21/18
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: portal
---

# Human Interface Devices Reference



Overview of the Human Interface Devices Reference technology.

To develop Human Interface Devices Reference, you need these headers:

 * [dinput.h](..\dinput\index.md)
 * [dinputd.h](..\dinputd\index.md)
 * [ntddkbd.h](..\ntddkbd\index.md)
 * [ntddmou.h](..\ntddmou\index.md)

For the programming guide, see [Human Interface Devices Reference](https://review.docs.microsoft.com/en-us/win32-test/hid).

## Structures

| Title   | Description   |
| ---- |:---- |
| [DIDEVICESTATE structure](..\dinputd\ns-dinputd-didevicestate.md) | The DIDEVICESTATE structure returns information about the state of a force feedback device. |
| [DIDRIVERVERSIONS structure](..\dinputd\ns-dinputd-didriverversions.md) | The DIDRIVERVERSIONS structure is used by the DirectInput effect driver to report version information back to DirectInput. |
| [DIEFFECTATTRIBUTES structure](..\dinputd\ns-dinputd-dieffectattributes.md) | The DIEFFECTATTRIBUTES structure describes the information contained in the &#0034;Attributes&#0034; value of the registry key for each effect that is supported by a force-feedback device. |
| [DIEFFESCAPE structure](..\dinput\ns-dinput-dieffescape.md) | The DIEFFESCAPE structure passes hardware-specific data directly to the device driver. |
| [DIFFDEVICEATTRIBUTES structure](..\dinputd\ns-dinputd-diffdeviceattributes.md) | The DIFFDEVICEATTRIBUTES structure describes the information contained in the &#0034;Attributes&#0034; value of the OEMForceFeedback registry key. |
| [DIFFOBJECTATTRIBUTES structure](..\dinputd\ns-dinputd-diffobjectattributes.md) | The DIFFOBJECTATTRIBUTES structure describes the information contained in the &#0034;FFAttributes&#0034; value of the registry key for each &#0034;object&#0034; on a force-feedback device. |
| [DIHIDFFINITINFO structure](..\dinputd\ns-dinputd-dihidffinitinfo.md) | The DIHIDFFINITINFO structure is used by DirectInput to provide information to a HID force-feedback driver about the device it is being asked to control. |
| [DIJOYCONFIG structure](..\dinputd\ns-dinputd-dijoyconfig.md) | The DIJOYCONFIG structure contains information about a joystick's configuration. |
| [DIJOYTYPEINFO structure](..\dinputd\ns-dinputd-dijoytypeinfo.md) | The DIJOYTYPEINFO structure contains information about a joystick type. |
| [DIJOYUSERVALUES structure](..\dinputd\ns-dinputd-dijoyuservalues.md) | The DIJOYUSERVALUES structure contains information about the user's joystick settings. |
| [DIOBJECTATTRIBUTES structure](..\dinputd\ns-dinputd-diobjectattributes.md) | The DIOBJECTATTRIBUTES structure describes the information contained in the &#0034;Attributes&#0034; value of the registry key for each &#0034;object&#0034; on a device. If the &#0034;Attributes&#0034; value is absent, then default attributes are used. |
| [DIOBJECTCALIBRATION structure](..\dinputd\ns-dinputd-diobjectcalibration.md) | The DIOBJECTCALIBRATION structure describes the information contained in the &#0034;Calibration&#0034; value of the registry key for each axis on a device. |
| [_KEYBOARD_ATTRIBUTES structure](..\ntddkbd\ns-ntddkbd-_keyboard_attributes.md) | KEYBOARD_ATTRIBUTES specifies the attributes of a keyboard. |
| [_KEYBOARD_INDICATOR_PARAMETERS structure](..\ntddkbd\ns-ntddkbd-_keyboard_indicator_parameters.md) | KEYBOARD_INDICATOR_PARAMETERS specifies the state of a keyboard's indicator LEDs. |
| [_KEYBOARD_INDICATOR_TRANSLATION structure](..\ntddkbd\ns-ntddkbd-_keyboard_indicator_translation.md) | KEYBOARD_INDICATOR_TRANSLATION specifies a device-specific, variable length array of mappings between keyboard scan codes and LED indicators. |
| [_KEYBOARD_INPUT_DATA structure](..\ntddkbd\ns-ntddkbd-_keyboard_input_data.md) | KEYBOARD_INPUT_DATA contains one packet of keyboard input data. |
| [_KEYBOARD_TYPEMATIC_PARAMETERS structure](..\ntddkbd\ns-ntddkbd-_keyboard_typematic_parameters.md) | KEYBOARD_TYPEMATIC_PARAMETERS specifies a keyboard's typematic settings. |
| [_KEYBOARD_UNIT_ID_PARAMETER structure](..\ntddkbd\ns-ntddkbd-_keyboard_unit_id_parameter.md) | KEYBOARD_UNIT_ID_PARAMETER specifies the unit ID that Kbdclass assigns to a keyboard. |
| [_MOUSE_ATTRIBUTES structure](..\ntddmou\ns-ntddmou-_mouse_attributes.md) | MOUSE_ATTRIBUTES specifies the attributes of a mouse device. |
| [_MOUSE_INPUT_DATA structure](..\ntddmou\ns-ntddmou-_mouse_input_data.md) | MOUSE_INPUT_DATA contains one packet of mouse input data. |
| [_MOUSE_UNIT_ID_PARAMETER structure](..\ntddmou\ns-ntddmou-_mouse_unit_id_parameter.md) | MOUSE_UNIT_ID_PARAMETER specifies a unit ID that Mouclass assigns to a mouse. |

## I/O control codes

| Title   | Description   |
| ---- |:---- |
| [IOCTL_KEYBOARD_QUERY_ATTRIBUTES IOCTL](..\ntddkbd\ni-ntddkbd-ioctl_keyboard_query_attributes.md) | The IOCTL_KEYBOARD_QUERY_ATTRIBUTES request returns information about the keyboard attributes. |
| [IOCTL_KEYBOARD_QUERY_INDICATORS IOCTL](..\ntddkbd\ni-ntddkbd-ioctl_keyboard_query_indicators.md) | The IOCTL_KEYBOARD_QUERY_INDICATORS request returns information about the keyboard indicators. |
| [IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION IOCTL](..\ntddkbd\ni-ntddkbd-ioctl_keyboard_query_indicator_translation.md) | The IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION request returns information about the mapping between scan codes and indicators. |
| [IOCTL_KEYBOARD_QUERY_TYPEMATIC IOCTL](..\ntddkbd\ni-ntddkbd-ioctl_keyboard_query_typematic.md) | The IOCTL_KEYBOARD_QUERY_TYPEMATIC request returns the typematic settings. |
| [IOCTL_KEYBOARD_SET_INDICATORS IOCTL](..\ntddkbd\ni-ntddkbd-ioctl_keyboard_set_indicators.md) | The IOCTL_KEYBOARD_SET_INDICATORS request sets the keyboard indicators. |
| [IOCTL_KEYBOARD_SET_TYPEMATIC IOCTL](..\ntddkbd\ni-ntddkbd-ioctl_keyboard_set_typematic.md) | The IOCTL_KEYBOARD_SET_TYPEMATIC request sets the typematic parameters. |
| [IOCTL_MOUSE_QUERY_ATTRIBUTES IOCTL](..\ntddmou\ni-ntddmou-ioctl_mouse_query_attributes.md) | The IOCTL_MOUSE_QUERY_ATTRIBUTES request returns information about the mouse attributes. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IDirectInputEffectDriver interface](..\dinputd\nn-dinputd-idirectinputeffectdriver.md) | These three methods allow additional interfaces to be added to the DirectInputEffectDriver object without affecting the functionality of the original interface. |
| [IDirectInputJoyConfig8 interface](..\dinputd\nn-dinputd-idirectinputjoyconfig8.md) | IDirectInputJoyConfig8 interface contains methods that allow hardware developers who are writing property sheets to write and read information to and from the registry. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IDirectInputEffectDriver::AddRef](..\dinputd\nf-dinputd-idirectinputeffectdriver-addref.md) | The IDirectInputEffectDriver |
| [IDirectInputEffectDriver::DestroyEffect](..\dinputd\nf-dinputd-idirectinputeffectdriver-destroyeffect.md) | The IDirectInputEffectDriver |
| [IDirectInputEffectDriver::DeviceID](..\dinputd\nf-dinputd-idirectinputeffectdriver-deviceid.md) | The IDirectInputEffectDriver |
| [IDirectInputEffectDriver::DownloadEffect](..\dinputd\nf-dinputd-idirectinputeffectdriver-downloadeffect.md) | The IDirectInputEffectDriver |
| [IDirectInputEffectDriver::Escape](..\dinputd\nf-dinputd-idirectinputeffectdriver-escape.md) | The IDirectInputEffectDriver |
| [IDirectInputEffectDriver::GetEffectStatus](..\dinputd\nf-dinputd-idirectinputeffectdriver-geteffectstatus.md) | The IDirectInputEffectDriver |
| [IDirectInputEffectDriver::GetForceFeedbackState](..\dinputd\nf-dinputd-idirectinputeffectdriver-getforcefeedbackstate.md) | The IDirectInputEffectDriver |
| [IDirectInputEffectDriver::GetVersions](..\dinputd\nf-dinputd-idirectinputeffectdriver-getversions.md) | The IDirectInputEffectDriver |
| [IDirectInputEffectDriver::QueryInterface](..\dinputd\nf-dinputd-idirectinputeffectdriver-queryinterface.md) | The IDirectInputEffectDriver |
| [IDirectInputEffectDriver::Release](..\dinputd\nf-dinputd-idirectinputeffectdriver-release.md) | The IDirectInputEffectDriver |
| [IDirectInputEffectDriver::SendForceFeedbackCommand](..\dinputd\nf-dinputd-idirectinputeffectdriver-sendforcefeedbackcommand.md) | The IDirectInputEffectDriver |
| [IDirectInputEffectDriver::SetGain](..\dinputd\nf-dinputd-idirectinputeffectdriver-setgain.md) | The IDirectInputEffectDriver |
| [IDirectInputEffectDriver::StartEffect](..\dinputd\nf-dinputd-idirectinputeffectdriver-starteffect.md) | The IDirectInputEffectDriver |
| [IDirectInputEffectDriver::StopEffect](..\dinputd\nf-dinputd-idirectinputeffectdriver-stopeffect.md) | The IDirectInputEffectDriver |
| [IDirectInputJoyConfig8::Acquire](..\dinputd\nf-dinputd-idirectinputjoyconfig8-acquire.md) | The IDirectInputJoyConfig8 |
| [IDirectInputJoyConfig8::AddNewHardware](..\dinputd\nf-dinputd-idirectinputjoyconfig8-addnewhardware.md) | The IDirectInputJoyConfig8 |
| [IDirectInputJoyConfig8::AddRef](..\dinputd\nf-dinputd-idirectinputjoyconfig8-addref.md) | The IDirectInputJoyConfig8 |
| [IDirectInputJoyConfig8::DeleteConfig](..\dinputd\nf-dinputd-idirectinputjoyconfig8-deleteconfig.md) | The IDirectInputJoyConfig8 |
| [IDirectInputJoyConfig8::DeleteType](..\dinputd\nf-dinputd-idirectinputjoyconfig8-deletetype.md) | The IDirectInputJoyConfig8 |
| [IDirectInputJoyConfig8::EnumTypes](..\dinputd\nf-dinputd-idirectinputjoyconfig8-enumtypes.md) | The IDirectInputJoyConfig8 |
| [IDirectInputJoyConfig8::GetConfig](..\dinputd\nf-dinputd-idirectinputjoyconfig8-getconfig.md) | The IDirectInputJoyConfig8 |
| [IDirectInputJoyConfig8::GetTypeInfo](..\dinputd\nf-dinputd-idirectinputjoyconfig8-gettypeinfo.md) | The IDirectInputJoyConfig8 |
| [IDirectInputJoyConfig8::GetUserValues](..\dinputd\nf-dinputd-idirectinputjoyconfig8-getuservalues.md) | The IDirectInputJoyConfig8 |
| [IDirectInputJoyConfig8::OpenAppStatusKey](..\dinputd\nf-dinputd-idirectinputjoyconfig8-openappstatuskey.md) | The IDirectInputJoyConfig8 |
| [IDirectInputJoyConfig8::OpenTypeKey](..\dinputd\nf-dinputd-idirectinputjoyconfig8-opentypekey.md) | The IDirectInputJoyConfig8 |
| [IDirectInputJoyConfig8::QueryInterface](..\dinputd\nf-dinputd-idirectinputjoyconfig8-queryinterface.md) | The IDirectInputJoyConfig8 |
| [IDirectInputJoyConfig8::Release](..\dinputd\nf-dinputd-idirectinputjoyconfig8-release.md) | The IDirectInputJoyConfig8 |
| [IDirectInputJoyConfig8::SendNotify](..\dinputd\nf-dinputd-idirectinputjoyconfig8-sendnotify.md) | The IDirectInputJoyConfig8 |
| [IDirectInputJoyConfig8::SetConfig](..\dinputd\nf-dinputd-idirectinputjoyconfig8-setconfig.md) | The IDirectInputJoyConfig8 |
| [IDirectInputJoyConfig8::SetCooperativeLevel](..\dinputd\nf-dinputd-idirectinputjoyconfig8-setcooperativelevel.md) | The IDirectInputJoyConfig8 |
| [IDirectInputJoyConfig8::SetTypeInfo](..\dinputd\nf-dinputd-idirectinputjoyconfig8-settypeinfo.md) | The IDirectInputJoyConfig8 |
| [IDirectInputJoyConfig8::SetUserValues](..\dinputd\nf-dinputd-idirectinputjoyconfig8-setuservalues.md) | The IDirectInputJoyConfig8 |
| [IDirectInputJoyConfig8::Unacquire](..\dinputd\nf-dinputd-idirectinputjoyconfig8-unacquire.md) | The IDirectInputJoyConfig8 |
