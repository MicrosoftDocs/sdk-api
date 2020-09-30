---
UID: NS:dinputd.DIJOYTYPEINFO
title: DIJOYTYPEINFO (dinputd.h)
description: The DIJOYTYPEINFO structure contains information about a joystick type.
helpviewer_keywords: ["*LPDIJOYTYPEINFO","DIJOYTYPEINFO","DIJOYTYPEINFO structure [Human Input Devices]","DIJOYTYPEINFO","*LPDIJOYTYPEINFO","DIJOYTYPEINFO","*LPDIJOYTYPEINFO structure [Human Input Devices]","di_ref_5b0a815b-710c-4f46-afa7-b8d051c7a5d6.xml","dinputd/DIJOYTYPEINFO","hid.dijoytypeinfo"]
old-location: hid\dijoytypeinfo.htm
tech.root: hid
ms.assetid: 54f52839-59ed-4edd-8d28-e3504f9900d0
ms.date: 12/05/2018
ms.keywords: '*LPDIJOYTYPEINFO, DIJOYTYPEINFO, DIJOYTYPEINFO structure [Human Input Devices], DIJOYTYPEINFO,*LPDIJOYTYPEINFO, DIJOYTYPEINFO,*LPDIJOYTYPEINFO structure [Human Input Devices], di_ref_5b0a815b-710c-4f46-afa7-b8d051c7a5d6.xml, dinputd/DIJOYTYPEINFO, hid.dijoytypeinfo'
req.header: dinputd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DIJOYTYPEINFO, *LPDIJOYTYPEINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DIJOYTYPEINFO
 - dinputd/DIJOYTYPEINFO
 - LPDIJOYTYPEINFO
 - dinputd/LPDIJOYTYPEINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dinputd.h
api_name:
 - DIJOYTYPEINFO, *LPDIJOYTYPEINFO
---

# DIJOYTYPEINFO structure


## -description

The <b>DIJOYTYPEINFO</b> structure contains information about a joystick type.

## -struct-fields

### -field dwSize

Specifies the size of the structure in bytes. This member must be initialized before the structure is used.

### -field hws

Joystick hardware settings.

### -field clsidConfig

Specifies a CLSID for the joystick type configuration object. Pass this CLSID to CoCreateInstance to create a configuration object. This field is zero if the type does not have custom configuration.

### -field wszDisplayName

The display name for the joystick type. The display name is the name that should be used to display the name of the joystick type to the end user.

### -field wszCallout

The device responsible for handling polling for devices of this type. This is a null string if the global polling callout is to be used.

### -field wszHardwareId

The hardware ID for the joystick type. The hardware ID is used by Plug and Play on Windows 2000 and Windows 98 (DirectX 7.0 only) to find the drivers for the joystick.

### -field dwFlags1

Joystick type flags. This member can be set to a combination of the following flags.





#### JOYTYPE_ZEROGAMEENUMOEMDATA

Zero GameEnum's OEM data field.



#### JOYTYPE_NOAUTODETECTGAMEPORT

Device does not support Autodetect gameport.



#### JOYTYPE_NOHIDDIRECT

Do not use HID directly for this device. (Windows 98 only.)



#### JOYTYPE_DEFAULTPROPSHEET

CPL overrides custom property sheet.

### -field dwFlags2

Combination of device filtering and device type/subtype override flags. Device-filtering flags should be placed in the high WORD of <b>dwFlags2</b>. Device type and subtype should be placed in the low and high WORDs of the member, respectively.





#### Device Filtering Flags

Hide unclassified devices.



#### JOYTYPE_MOUSEHIDE

Hide mice.



#### JOYTYPE_KEYBHIDE

Hide keyboards.



#### JOYTYPE_GAMEHIDE

Hide game controllers.



#### JOYTYPE_HIDEACTIVE

Hide flags are active. This flag must be included if any other hide flags are specified.



#### Device Type and Subtype Override Flags

<table>
<tr>
<th>Device Type</th>
<th>Device Subtype</th>
</tr>
<tr>
<td>
DI8DEVTYPE_1STPERSON

</td>
<td>
DI8DEVTYPE1STPERSON_LIMITED

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPE1STPERSON_UNKNOWN

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPE1STPERSON_SIXDOF

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPE1STPERSON_SHOOTER

</td>
</tr>
<tr>
<td>
DI8DEVTYPE_DEVICE

</td>
<td>
n/a

</td>
</tr>
<tr>
<td>
DI8DEVTYPE_DEVICECTRL

</td>
<td>
DI8DEVTYPEDEVICECTRL_UNKNOWN

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEDEVICECTRL_COMMSSELECTION

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEDEVICECTRL_COMMSSELECTION_HARDWIRED

</td>
</tr>
<tr>
<td>
DI8DEVTYPE_DRIVING

</td>
<td>
DI8DEVTYPEDRIVING_LIMITED

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEDRIVING_COMBINEDPEDALS

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEDRIVING_DUALPEDALS

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEDRIVING_THREEPEDALS

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEDRIVING_HANDHELD

</td>
</tr>
<tr>
<td>
DI8DEVTYPE_FLIGHT

</td>
<td>
DI8DEVTYPEFLIGHT_LIMITED

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEFLIGHT_STICK

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEFLIGHT_YOKE

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEFLIGHT_RC

</td>
</tr>
<tr>
<td>
DI8DEVTYPE_GAMEPAD

</td>
<td>
DI8DEVTYPEGAMEPAD_LIMITED

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEGAMEPAD_STANDARD

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEGAMEPAD_TILT

</td>
</tr>
<tr>
<td>
DI8DEVTYPE_JOYSTICK

</td>
<td>
DI8DEVTYPEJOYSTICK_LIMITED

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEJOYSTICK_STANDARD

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEJOYSTICK_ENHANCED

</td>
</tr>
<tr>
<td>
DI8DEVTYPE_KEYBOARD

</td>
<td>
DI8DEVTYPEKEYBOARD_UNKNOWN

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEKEYBOARD_PCXT

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEKEYBOARD_OLIVETTI

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEKEYBOARD_PCAT

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEKEYBOARD_PCENH

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEKEYBOARD_NOKIA1050

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEKEYBOARD_NOKIA9140

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEKEYBOARD_NEC98

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEKEYBOARD_NEC98LAPTOP

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEKEYBOARD_NEC98106

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEKEYBOARD_JAPAN106

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEKEYBOARD_JAPANAX

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEKEYBOARD_J3100

</td>
</tr>
<tr>
<td>
DI8DEVTYPE_MOUSE

</td>
<td>
DI8DEVTYPEMOUSE_UNKNOWN

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEMOUSE_TRADITIONAL

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEMOUSE_FINGERSTICK

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEMOUSE_TOUCHPAD

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEMOUSE_TRACKBALL

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPEMOUSE_ABSOLUTE

</td>
</tr>
<tr>
<td>
DI8DEVTYPE_REMOTE

</td>
<td>
DI8DEVTYPEREMOTE_UNKNOWN

</td>
</tr>
<tr>
<td>
DI8DEVTYPE_SCREENPOINTER

</td>
<td>
DI8DEVTYPESCREENPTR_UNKNOWN

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPESCREENPTR_LIGHTGUN

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPESCREENPTR_LIGHTPEN

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPESCREENPTR_TOUCH

</td>
</tr>
<tr>
<td>
DI8DEVTYPE_SUPPLEMENTAL

</td>
<td>
DI8DEVTYPESUPPLEMENTAL_UNKNOWN

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPESUPPLEMENTAL_2NDHANDCONTROLLER

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPESUPPLEMENTAL_HEADTRACKER

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPESUPPLEMENTAL_HANDTRACKER

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPESUPPLEMENTAL_SHIFTSTICKGATE

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPESUPPLEMENTAL_SHIFTER

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPESUPPLEMENTAL_THROTTLE

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPESUPPLEMENTAL_SPLITTHROTTLE

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPESUPPLEMENTAL_COMBINEDPEDALS

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPESUPPLEMENTAL_DUALPEDALS

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPESUPPLEMENTAL_THREEPEDALS

</td>
</tr>
<tr>
<td></td>
<td>
DI8DEVTYPESUPPLEMENTAL_RUDDERPEDALS

</td>
</tr>
</table>

### -field wszMapFile

## -remarks

A "joystick type" describes how DirectInput should communicate with the device and how it should report device data. For example, "A Frobozz Industries SuperStick 5X is a three-axis, five-button joystick with the third axis reported as the first bit on the second port." 

DirectInput comes with the following predefined joystick types, all with axes in their default locations:

<ul>
<li>
Two-axis, two-button joystick. 

</li>
<li>
Two-button game pad. 

</li>
<li>
Two-button flight yoke. 

</li>
<li>
Two-button flight yoke with throttle. 

</li>
<li>
Three-axis, two-button joystick. 

</li>
<li>
Three-axis, four-button joystick. 

</li>
<li>
Four-button game pad. 

</li>
<li>
Four-button flight yoke. 

</li>
<li>
Four-button flight yoke with throttle. 

</li>
</ul>
If the joystick type has the JOY_HWS_ISGAMEPORTDRIVER flag set in the <b>dwFlags</b> member of the JOYHWSETTINGS structure, then the <b>wszCallout</b> member of the DIJOYTYPEINFO structure contains the name of a driver that can be used as a global driver. The joystick type should be shown on the list of global drivers and not shown on the list of joystick types that can be assigned. 

<b>New in DirectX 8.0</b>

The <b>dwFlags2</b> member was added to the DIJOYCONFIG structure. This member carries information that controls how DirectInput enumerates the device to applications. The <b>dwFlags2</b> member carries device type and subtype override flags in the low word, and device enumeration "hiding" flags in the high word. The device type and subtype override flags control how DirectInput portrays your device to applications that use DirectInput. These are the same flags that applications receive from DirectInput during device enumeration. For example, if your device is described in its firmware as a telephony device, it would not normally be enumerated to games because telephony devices aren't considered relevant to games. However, if you used DI8DEVTYPE_DEVICECTRL and DI8DEVTYPEDEVICECONTROL_COMMSSELECTION to describe this device, DirectInput overrides the data it retrieves from the firmware and enumerates the device to games.

The high word of <b>dwFlags2</b> can be set to contain flags that scope how DirectInput enumerates the device to DirectInput applications. For example, some devices declare multiple top-level HID collections. Such a device might declare that it can act as a keyboard, a mouse, and a joystick all in one. Generally, one or more of these top-level collections is merely a phantom device, which shouldn't be enumerated to games. For this device, the high word of <b>dwFlags2</b> could be set to a combination of the JOYTYPE_HIDEACTIVE, JOYTYPE_MOUSEHIDE, and JOYTYPE_KEYBHIDE flags. The JOYTYPE_HIDEACTIVE flag indicates that DirectInput should not enumerate the device by all its types. The JOYTYPE_MOUSEHIDE and JOYTYPE_KEYBHIDE flags also present in the high word indicate to DirectInput that enumeration of the phantom mouse and keyboard on the device should be suppressed. Note that applications can include the DIEDFL_INCLUDEHIDDEN (described in the Microsoft Windows SDK documentation) flag to enumerate devices, even if they are hidden.

