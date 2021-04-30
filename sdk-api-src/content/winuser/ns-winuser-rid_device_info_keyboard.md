---
UID: NS:winuser.tagRID_DEVICE_INFO_KEYBOARD
title: RID_DEVICE_INFO_KEYBOARD (winuser.h)
description: Defines the raw input data coming from the specified keyboard.
helpviewer_keywords: ["*PRID_DEVICE_INFO_KEYBOARD","PRID_DEVICE_INFO_KEYBOARD","PRID_DEVICE_INFO_KEYBOARD structure pointer [Keyboard and Mouse Input]","RID_DEVICE_INFO_KEYBOARD","RID_DEVICE_INFO_KEYBOARD structure [Keyboard and Mouse Input]","_win32_RID_DEVICE_INFO_KEYBOARD_str","_win32_rid_device_info_keyboard_str_cpp","inputdev.rid_device_info_keyboard","winui._win32_rid_device_info_keyboard_str","winuser/PRID_DEVICE_INFO_KEYBOARD","winuser/RID_DEVICE_INFO_KEYBOARD"]
old-location: inputdev\rid_device_info_keyboard.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputstructures\rid_device_info_keyboard.htm
ms.date: 02/25/2021
ms.keywords: '*PRID_DEVICE_INFO_KEYBOARD, PRID_DEVICE_INFO_KEYBOARD, PRID_DEVICE_INFO_KEYBOARD structure pointer [Keyboard and Mouse Input], RID_DEVICE_INFO_KEYBOARD, RID_DEVICE_INFO_KEYBOARD structure [Keyboard and Mouse Input], _win32_RID_DEVICE_INFO_KEYBOARD_str, _win32_rid_device_info_keyboard_str_cpp, inputdev.rid_device_info_keyboard, winui._win32_rid_device_info_keyboard_str, winuser/PRID_DEVICE_INFO_KEYBOARD, winuser/RID_DEVICE_INFO_KEYBOARD'
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: RID_DEVICE_INFO_KEYBOARD, *PRID_DEVICE_INFO_KEYBOARD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRID_DEVICE_INFO_KEYBOARD
 - winuser/tagRID_DEVICE_INFO_KEYBOARD
 - PRID_DEVICE_INFO_KEYBOARD
 - winuser/PRID_DEVICE_INFO_KEYBOARD
 - RID_DEVICE_INFO_KEYBOARD
 - winuser/RID_DEVICE_INFO_KEYBOARD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - RID_DEVICE_INFO_KEYBOARD
---

# RID_DEVICE_INFO_KEYBOARD structure


## -description

Defines the raw input data coming from the specified keyboard.

## -struct-fields

### -field dwType

Type: <b>DWORD</b>

The type of keyboard. See [Remarks](#remarks).

| Value | Description                                          |
|:-----:|------------------------------------------------------|
|  0x4  | Enhanced 101- or 102-key keyboards (and compatibles) |
|  0x7  | Japanese Keyboard                                    |
|  0x8  | Korean Keyboard                                      |
| 0x51  | Unknown type or HID keyboard                         |

### -field dwSubType

Type: <b>DWORD</b>

The vendor-specific subtype of the keyboard. See [Remarks](#remarks).

### -field dwKeyboardMode

Type: <b>DWORD</b>

The scan code mode. Usually 1, which means that *Scan Code Set 1* is used. See [Keyboard Scan Code Specification](https://download.microsoft.com/download/1/6/1/161ba512-40e2-4cc9-843a-923143f3456c/scancode.doc).

### -field dwNumberOfFunctionKeys

Type: <b>DWORD</b>

The number of function keys on the keyboard.

### -field dwNumberOfIndicators

Type: <b>DWORD</b>

The number of LED indicators on the keyboard.

### -field dwNumberOfKeysTotal

Type: <b>DWORD</b>

The total number of keys on the keyboard.

## -remarks

For information about keyboard types, subtypes, scan code modes, and related keyboard layouts, see the documentation in *kbd.h*, *ntdd8042.h* and *ntddkbd.h* headers in Windows SDK, and the [Keyboard Layout Samples](/samples/microsoft/windows-driver-samples/keyboard-layout-samples/).

## -see-also

**Conceptual**

[RID_DEVICE_INFO](ns-winuser-rid_device_info.md)

[Raw Input](/windows/desktop/inputdev/raw-input)

**Reference**

[KEYBOARD_ATTRIBUTES structure](../ntddkbd/ns-ntddkbd-keyboard_attributes.md)
