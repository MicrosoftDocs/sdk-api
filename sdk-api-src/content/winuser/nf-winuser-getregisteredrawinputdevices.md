---
UID: NF:winuser.GetRegisteredRawInputDevices
title: GetRegisteredRawInputDevices function
author: windows-sdk-content
description: Retrieves the information about the raw input devices for the current application.
old-location: inputdev\getregisteredrawinputdevices.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputfunctions\getregisteredrawinputdevices.htm
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: GetRegisteredRawInputDevices, GetRegisteredRawInputDevices function [Keyboard and Mouse Input], _win32_GetRegisteredRawInputDevices, _win32_getregisteredrawinputdevices_cpp, inputdev.getregisteredrawinputdevices, winui._win32_getregisteredrawinputdevices, winuser/GetRegisteredRawInputDevices
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: POINTER_DEVICE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - GetRegisteredRawInputDevices
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetRegisteredRawInputDevices function


## -description


Retrieves the information about the raw input devices for the current application.


## -parameters




### -param pRawInputDevices [out, optional]

Type: <b>PRAWINPUTDEVICE</b>

An array of <a href="https://msdn.microsoft.com/library/ms645565(v=VS.85).aspx">RAWINPUTDEVICE</a> structures for the application. 


### -param puiNumDevices [in, out]

Type: <b>PUINT</b>

The number of <a href="https://msdn.microsoft.com/library/ms645565(v=VS.85).aspx">RAWINPUTDEVICE</a> structures in *<i>pRawInputDevices</i>. 


### -param cbSize [in]

Type: <b>UINT</b>

The size, in bytes, of a <a href="https://msdn.microsoft.com/library/ms645565(v=VS.85).aspx">RAWINPUTDEVICE</a> structure. 


## -returns



Type: <b>UINT</b>

If successful, the function returns a non-negative number that is the number of <a href="https://msdn.microsoft.com/library/ms645565(v=VS.85).aspx">RAWINPUTDEVICE</a> structures written to the buffer. 

If the <i>pRawInputDevices</i> buffer is too small or <b>NULL</b>, the function sets the last error as <b>ERROR_INSUFFICIENT_BUFFER</b>, returns -1, and sets <i>puiNumDevices</i> to the required number of devices. If the function fails for any other reason, it returns -1. For more details, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



To receive raw input from a device, an application must register it by using <a href="https://msdn.microsoft.com/library/ms645600(v=VS.85).aspx">RegisterRawInputDevices</a>. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/ms645565(v=VS.85).aspx">RAWINPUTDEVICE</a>



<a href="https://msdn.microsoft.com/library/ms645536(v=VS.85).aspx">Raw Input</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/ms645600(v=VS.85).aspx">RegisterRawInputDevices</a>
 

 

