---
UID: NS:winuser.tagRAWINPUT
title: RAWINPUT (winuser.h)
description: Contains the raw input from a device.
helpviewer_keywords: ["*LPRAWINPUT","*PRAWINPUT","LPRAWINPUT","LPRAWINPUT structure pointer [Keyboard and Mouse Input]","PRAWINPUT","PRAWINPUT structure pointer [Keyboard and Mouse Input]","RAWINPUT","RAWINPUT structure [Keyboard and Mouse Input]","_win32_RAWINPUT_str","_win32_rawinput_str_cpp","inputdev.rawinput","winui._win32_rawinput_str","winuser/LPRAWINPUT","winuser/PRAWINPUT","winuser/RAWINPUT"]
old-location: inputdev\rawinput.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputstructures\rawinput.htm
ms.date: 12/05/2018
ms.keywords: '*LPRAWINPUT, *PRAWINPUT, LPRAWINPUT, LPRAWINPUT structure pointer [Keyboard and Mouse Input], PRAWINPUT, PRAWINPUT structure pointer [Keyboard and Mouse Input], RAWINPUT, RAWINPUT structure [Keyboard and Mouse Input], _win32_RAWINPUT_str, _win32_rawinput_str_cpp, inputdev.rawinput, winui._win32_rawinput_str, winuser/LPRAWINPUT, winuser/PRAWINPUT, winuser/RAWINPUT'
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
req.typenames: RAWINPUT, *PRAWINPUT, *LPRAWINPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRAWINPUT
 - winuser/tagRAWINPUT
 - PRAWINPUT
 - winuser/PRAWINPUT
 - RAWINPUT
 - winuser/RAWINPUT
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
 - RAWINPUT
---

# RAWINPUT structure


## -description

Contains the raw input from a device.

## -struct-fields

### -field header

Type: <b><a href="/windows/desktop/api/winuser/ns-winuser-rawinputheader">RAWINPUTHEADER</a></b>

The raw input data.

### -field data

### -field data.mouse

Type: <b><a href="/windows/desktop/api/winuser/ns-winuser-rawmouse">RAWMOUSE</a></b>

If the data comes from a mouse, this is the raw input data.

### -field data.keyboard

Type: <b><a href="/windows/desktop/api/winuser/ns-winuser-rawkeyboard">RAWKEYBOARD</a></b>

If the data comes from a keyboard, this is the raw input data.

### -field data.hid

Type: <b><a href="/windows/desktop/api/winuser/ns-winuser-rawhid">RAWHID</a></b>

If the data comes from an HID, this is the raw input data.

## -remarks

The handle to this structure is passed in the <i>lParam</i> parameter of <a href="/windows/desktop/inputdev/wm-input">WM_INPUT</a>.

To get detailed information -- such as the header and the content of the raw input -- call <a href="/windows/desktop/api/winuser/nf-winuser-getrawinputdata">GetRawInputData</a>.

To read the <b>RAWINPUT</b> in the message loop as a buffered read, call <a href="/windows/desktop/api/winuser/nf-winuser-getrawinputbuffer">GetRawInputBuffer</a>. 

To get device specific information, call <a href="/windows/desktop/api/winuser/nf-winuser-getrawinputdeviceinfoa">GetRawInputDeviceInfo</a> with the <i>hDevice</i> from <a href="/windows/desktop/api/winuser/ns-winuser-rawinputheader">RAWINPUTHEADER</a>.

Raw input is available only when the application calls <a href="/windows/desktop/api/winuser/nf-winuser-registerrawinputdevices">RegisterRawInputDevices</a> with valid device specifications.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getrawinputbuffer">GetRawInputBuffer</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getrawinputdata">GetRawInputData</a>



<a href="/windows/desktop/api/winuser/ns-winuser-rawhid">RAWHID</a>



<a href="/windows/desktop/api/winuser/ns-winuser-rawinputheader">RAWINPUTHEADER</a>



<a href="/windows/desktop/api/winuser/ns-winuser-rawkeyboard">RAWKEYBOARD</a>



<a href="/windows/desktop/api/winuser/ns-winuser-rawmouse">RAWMOUSE</a>



<a href="/windows/desktop/inputdev/raw-input">Raw Input</a>



<b>Reference</b>
