---
UID: NF:winuser.EnableMouseInPointer
title: EnableMouseInPointer function
author: windows-sdk-content
description: Enables the mouse to act as a pointer input device and send WM_POINTER messages.
old-location: inputmsg\enablemouseinpointer.htm
tech.root: InputMsg
ms.assetid: 66D9BF17-164F-455F-803F-36CDF88C34FF
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: EnableMouseInPointer, EnableMouseInPointer function [Keyboard and Mouse Input], inputdev.enablemouseinpointer, inputmsg.enablemouseinpointer, winuser/EnableMouseInPointer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - MinUser.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-0.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-1.dll
 - API-Ms-Win-RTCore-NTUser-WMPointer-L1-1-2.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-L1-1-3.dll
api_name:
 - EnableMouseInPointer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EnableMouseInPointer function


## -description


Enables the mouse to act as a pointer input device and send <a href="https://msdn.microsoft.com/65F4DCD0-DAE1-4AC2-AB36-23D114803138">WM_POINTER</a> messages.


## -parameters




### -param fEnable [in]

<b>TRUE</b> to turn on mouse input support in <a href="https://msdn.microsoft.com/65F4DCD0-DAE1-4AC2-AB36-23D114803138">WM_POINTER</a>.


## -returns



If the function succeeds, the return value is non-zero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function can be called only once in the context of a process lifetime.  Prior to the first call, Windows Store apps run with mouse-in-pointer enabled, as do any desktop applications that consume mshtml.dll.  All other desktop applications run with mouse-in-pointer disabled.

On the first call in the process lifetime, the state is changed as specified and the call succeeds.

On subsequent calls, the state will not change.  If the current state is not equal to the specified state, the call fails.

Call <a href="https://msdn.microsoft.com/5D493066-2425-4610-8489-575BF25C8C16">IsMouseInPointerEnabled</a> to verify the mouse-in-pointer state.




## -see-also




<a href="https://msdn.microsoft.com/0123DCD0-DAE1-4AC2-AB36-23D114803138">Functions</a>



<a href="https://msdn.microsoft.com/5D493066-2425-4610-8489-575BF25C8C16">IsMouseInPointerEnabled</a>



<a href="https://msdn.microsoft.com/65F4DCD0-DAE1-4AC2-AB36-23D114803138">WM_POINTER</a>
 

 

