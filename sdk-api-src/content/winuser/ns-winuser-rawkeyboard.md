---
UID: NS:winuser.tagRAWKEYBOARD
title: RAWKEYBOARD (winuser.h)
description: Contains information about the state of the keyboard.
old-location: inputdev\rawkeyboard.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputstructures\rawkeyboard.htm
ms.date: 12/05/2018
ms.keywords: '*LPRAWKEYBOARD, *PRAWKEYBOARD, LPRAWKEYBOARD, LPRAWKEYBOARD structure pointer [Keyboard and Mouse Input], PRAWKEYBOARD, PRAWKEYBOARD structure pointer [Keyboard and Mouse Input], RAWKEYBOARD, RAWKEYBOARD structure [Keyboard and Mouse Input], RI_KEY_BREAK, RI_KEY_E0, RI_KEY_E1, RI_KEY_MAKE, _win32_RAWKEYBOARD_str, _win32_rawkeyboard_str_cpp, inputdev.rawkeyboard, winui._win32_rawkeyboard_str, winuser/LPRAWKEYBOARD, winuser/PRAWKEYBOARD, winuser/RAWKEYBOARD'
f1_keywords:
- winuser/RAWKEYBOARD
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Winuser.h
api_name:
- RAWKEYBOARD
targetos: Windows
req.typenames: RAWKEYBOARD, *PRAWKEYBOARD, *LPRAWKEYBOARD
req.redist: 
ms.custom: 19H1
---

# RAWKEYBOARD structure

## -description

Contains information about the state of the keyboard. 

## -struct-fields

### -field MakeCode

Type: <b>USHORT</b>

Specifies the scan code (from Scan Code Set 1) associated with a key press. See Remarks.

### -field Flags

Type: <b>USHORT</b>

Flags for scan code information. It can be one or more of the following:

| Value                | Meaning                          |
|----------------------|----------------------------------|
| **RI\_KEY\_MAKE** 0  | The key is down.                 |
| **RI\_KEY\_BREAK** 1 | The key is up.                   |
| **RI\_KEY\_E0** 2    | The scan code has the E0 prefix. |
| **RI\_KEY\_E1** 4    | The scan code has the E1 prefix. |

### -field Reserved

Type: <b>USHORT</b>

Reserved; must be zero. 

### -field VKey

Type: <b>USHORT</b>

The corresponding [legacy virtual-key code](https://docs.microsoft.com/windows/win32/inputdev/virtual-key-codes).

### -field Message

Type: <b>UINT</b>

The corresponding [legacy keyboard window message](https://docs.microsoft.com/windows/win32/inputdev/keyboard-input-notifications), for example [WM_KEYDOWN](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown), [WM_SYSKEYDOWN](https://docs.microsoft.com/windows/win32/inputdev/wm-syskeydown), and so forth. 

### -field ExtraInformation

Type: <b>ULONG</b>

The device-specific additional information for the event.

## -remarks

For a **MakeCode** value [HID client mapper driver](https://docs.microsoft.com/windows-hardware/drivers/hid/keyboard-and-mouse-hid-client-drivers) converts HID usages into scan codes according to [USB HID to PS/2 Scan Code Translation Table](https://download.microsoft.com/download/1/6/1/161ba512-40e2-4cc9-843a-923143f3456c/translate.pdf) (see **PS/2 Set 1 Make** column).

Older PS/2 keyboards actually transmit Scan Code Set 2 values down the wire from the keyboard to the keyboard port. These values are translated to Scan Code Set 1 by the i8042 port chip. Possible values are listed in [Keyboard Scan Code Specification](http://download.microsoft.com/download/1/6/1/161ba512-40e2-4cc9-843a-923143f3456c/scancode.doc) (see **Scan Code Table**).

<b>KEYBOARD_OVERRUN_MAKE_CODE</b> is a special **MakeCode** value sent when an invalid or unrecognizable combination of keys is pressed or the number of keys pressed exceeds the limit for this keyboard.

## -see-also

<b>Conceptual</b>

[GetRawInputDeviceInfo](nf-winuser-getrawinputdeviceinfoa.md)

[RAWINPUT](ns-winuser-rawinput.md)

[Raw Input](https://docs.microsoft.com/windows/win32/inputdev/raw-input)

[Keyboard and mouse HID client drivers](https://docs.microsoft.com/windows-hardware/drivers/hid/keyboard-and-mouse-hid-client-drivers)

<b>Reference</b>

[USB HID to PS/2 Scan Code Translation Table](https://download.microsoft.com/download/1/6/1/161ba512-40e2-4cc9-843a-923143f3456c/translate.pdf)

[PS/2 Keyboard Scan Code Specification](http://download.microsoft.com/download/1/6/1/161ba512-40e2-4cc9-843a-923143f3456c/scancode.doc)

[KEYBOARD_INPUT_DATA structure](https://docs.microsoft.com/windows/win32/api/ntddkbd/ns-ntddkbd-keyboard_input_data)
