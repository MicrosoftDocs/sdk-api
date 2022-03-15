---
UID: NS:winuser.tagRAWINPUTHEADER
title: RAWINPUTHEADER (winuser.h)
description: Contains the header information that is part of the raw input data.
helpviewer_keywords: ["*LPRAWINPUTHEADER","*PRAWINPUTHEADER","PRAWINPUTHEADER","PRAWINPUTHEADER structure pointer [Keyboard and Mouse Input]","RAWINPUTHEADER","RAWINPUTHEADER structure [Keyboard and Mouse Input]","RIM_TYPEHID","RIM_TYPEKEYBOARD","RIM_TYPEMOUSE","_win32_RAWINPUTHEADER_str","_win32_rawinputheader_str_cpp","inputdev.rawinputheader","winui._win32_rawinputheader_str","winuser/PRAWINPUTHEADER","winuser/RAWINPUTHEADER"]
old-location: inputdev\rawinputheader.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputstructures\rawinputheader.htm
ms.date: 12/05/2018
ms.keywords: '*LPRAWINPUTHEADER, *PRAWINPUTHEADER, PRAWINPUTHEADER, PRAWINPUTHEADER structure pointer [Keyboard and Mouse Input], RAWINPUTHEADER, RAWINPUTHEADER structure [Keyboard and Mouse Input], RIM_TYPEHID, RIM_TYPEKEYBOARD, RIM_TYPEMOUSE, _win32_RAWINPUTHEADER_str, _win32_rawinputheader_str_cpp, inputdev.rawinputheader, winui._win32_rawinputheader_str, winuser/PRAWINPUTHEADER, winuser/RAWINPUTHEADER'
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
req.typenames: RAWINPUTHEADER, *PRAWINPUTHEADER, *LPRAWINPUTHEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRAWINPUTHEADER
 - winuser/tagRAWINPUTHEADER
 - PRAWINPUTHEADER
 - winuser/PRAWINPUTHEADER
 - RAWINPUTHEADER
 - winuser/RAWINPUTHEADER
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
 - RAWINPUTHEADER
---

# RAWINPUTHEADER structure


## -description

Contains the header information that is part of the raw input data.

## -struct-fields

### -field dwType

Type: <b>DWORD</b>

The type of raw input. It can be one of the following values:

| Value                   | Meaning                                                             |
|-------------------------|---------------------------------------------------------------------|
| **RIM\_TYPEMOUSE** 0    | Raw input comes from the mouse.                                     |
| **RIM\_TYPEKEYBOARD** 1 | Raw input comes from the keyboard.                                  |
| **RIM\_TYPEHID** 2      | Raw input comes from some device that is not a keyboard or a mouse. |

### -field dwSize

Type: <b>DWORD</b>

The size, in bytes, of the entire input packet of data. This includes [RAWINPUT](ns-winuser-rawinput.md) plus possible extra input reports in the [RAWHID](ns-winuser-rawhid.md) variable length array.

### -field hDevice

Type: <b>HANDLE</b>

A handle to the device generating the raw input data.

### -field wParam

Type: <b>WPARAM</b>

The value passed in the <i>wParam</i> parameter of the [WM_INPUT](/windows/win32/inputdev/wm-input) message.

## -remarks

To get more information on the device, use <b>hDevice</b> in a call to [GetRawInputDeviceInfo](nf-winuser-getrawinputdeviceinfoa.md). <b>hDevice</b> can be zero if an input is received from a precision touchpad.

## -see-also

<b>Conceptual</b>

[GetRawInputDeviceInfo](nf-winuser-getrawinputdeviceinfoa.md)

[RAWINPUT structure](ns-winuser-rawinput.md)

[RAWKEYBOARD structure](ns-winuser-rawkeyboard.md)

[RAWMOUSE structure](ns-winuser-rawmouse.md)

[RAWHID structure](ns-winuser-rawhid.md)

[Raw Input](/windows/win32/inputdev/raw-input)

<b>Reference</b>

[WM_INPUT](/windows/win32/inputdev/wm-input)
