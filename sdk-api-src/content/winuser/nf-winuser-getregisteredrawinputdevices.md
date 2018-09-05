---
UID: NF:winuser.GetRegisteredRawInputDevices
title: GetRegisteredRawInputDevices function
author: windows-sdk-content
description: Retrieves the information about the raw input devices for the current application.
old-location: inputdev\getregisteredrawinputdevices.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputfunctions\getregisteredrawinputdevices.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetRegisteredRawInputDevices, GetRegisteredRawInputDevices function [Keyboard and Mouse Input], _win32_GetRegisteredRawInputDevices, _win32_getregisteredrawinputdevices_cpp, inputdev.getregisteredrawinputdevices, winui._win32_getregisteredrawinputdevices, winuser/GetRegisteredRawInputDevices
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
req.typenames: 
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

An array of <a href="https://msdn.microsoft.com/c8f97d22-2aeb-4aa9-a015-5b13d936899d">RAWINPUTDEVICE</a> structures for the application. 


### -param puiNumDevices [in, out]

Type: <b>PUINT</b>

The number of <a href="https://msdn.microsoft.com/c8f97d22-2aeb-4aa9-a015-5b13d936899d">RAWINPUTDEVICE</a> structures in *<i>pRawInputDevices</i>. 


### -param cbSize [in]

Type: <b>UINT</b>

The size, in bytes, of a <a href="https://msdn.microsoft.com/c8f97d22-2aeb-4aa9-a015-5b13d936899d">RAWINPUTDEVICE</a> structure. 


## -returns



Type: <b>UINT</b>

If successful, the function returns a non-negative number that is the number of <a href="https://msdn.microsoft.com/c8f97d22-2aeb-4aa9-a015-5b13d936899d">RAWINPUTDEVICE</a> structures written to the buffer. 

If the <i>pRawInputDevices</i> buffer is too small or <b>NULL</b>, the function sets the last error as <b>ERROR_INSUFFICIENT_BUFFER</b>, returns -1, and sets <i>puiNumDevices</i> to the required number of devices. If the function fails for any other reason, it returns -1. For more details, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



To receive raw input from a device, an application must register it by using <a href="https://msdn.microsoft.com/abf60a07-5d82-4737-96df-b76c9c449261">RegisterRawInputDevices</a>. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/c8f97d22-2aeb-4aa9-a015-5b13d936899d">RAWINPUTDEVICE</a>



<a href="https://msdn.microsoft.com/a2afdb80-d68a-4c33-826f-96739d239cd9">Raw Input</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/abf60a07-5d82-4737-96df-b76c9c449261">RegisterRawInputDevices</a>
 

 

