---
UID: NF:winuser.GetRegisteredRawInputDevices
title: GetRegisteredRawInputDevices function (winuser.h)
description: Retrieves the information about the raw input devices for the current application.
helpviewer_keywords: ["GetRegisteredRawInputDevices","GetRegisteredRawInputDevices function [Keyboard and Mouse Input]","_win32_GetRegisteredRawInputDevices","_win32_getregisteredrawinputdevices_cpp","inputdev.getregisteredrawinputdevices","winui._win32_getregisteredrawinputdevices","winuser/GetRegisteredRawInputDevices"]
old-location: inputdev\getregisteredrawinputdevices.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputfunctions\getregisteredrawinputdevices.htm
ms.date: 12/05/2018
ms.keywords: GetRegisteredRawInputDevices, GetRegisteredRawInputDevices function [Keyboard and Mouse Input], _win32_GetRegisteredRawInputDevices, _win32_getregisteredrawinputdevices_cpp, inputdev.getregisteredrawinputdevices, winui._win32_getregisteredrawinputdevices, winuser/GetRegisteredRawInputDevices
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetRegisteredRawInputDevices
 - winuser/GetRegisteredRawInputDevices
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - GetRegisteredRawInputDevices
---

# GetRegisteredRawInputDevices function


## -description

Retrieves the information about the raw input devices for the current application.

## -parameters

### -param pRawInputDevices [out, optional]

Type: <b>PRAWINPUTDEVICE</b>

An array of <a href="/windows/desktop/api/winuser/ns-winuser-rawinputdevice">RAWINPUTDEVICE</a> structures for the application. Pointer should be aligned on a **DWORD** (32-bit) boundary.

### -param puiNumDevices [in, out]

Type: <b>PUINT</b>

The number of <a href="/windows/desktop/api/winuser/ns-winuser-rawinputdevice">RAWINPUTDEVICE</a> structures in *<i>pRawInputDevices</i>.

### -param cbSize [in]

Type: <b>UINT</b>

The size, in bytes, of a <a href="/windows/desktop/api/winuser/ns-winuser-rawinputdevice">RAWINPUTDEVICE</a> structure.

## -returns

Type: <b>UINT</b>

If successful, the function returns a non-negative number that is the number of <a href="/windows/desktop/api/winuser/ns-winuser-rawinputdevice">RAWINPUTDEVICE</a> structures written to the buffer. 

If the <i>pRawInputDevices</i> buffer is too small or <b>NULL</b>, the function sets the last error as <b>ERROR_INSUFFICIENT_BUFFER</b>, returns -1, and sets <i>puiNumDevices</i> to the required number of devices. If the function fails for any other reason, it returns -1. For more details, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To receive raw input from a device, an application must register it by using <a href="/windows/desktop/api/winuser/nf-winuser-registerrawinputdevices">RegisterRawInputDevices</a>.

## -see-also

<b>Conceptual</b>

<a href="/windows/desktop/api/winuser/ns-winuser-rawinputdevice">RAWINPUTDEVICE</a>

<a href="/windows/desktop/inputdev/raw-input">Raw Input</a>

<b>Reference</b>

<a href="/windows/desktop/api/winuser/nf-winuser-registerrawinputdevices">RegisterRawInputDevices</a>
