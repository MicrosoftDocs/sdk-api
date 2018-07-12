---
UID: NF:winuser.IsMouseInPointerEnabled
title: IsMouseInPointerEnabled function
author: windows-sdk-content
description: Indicates whether EnableMouseInPointer is set for the mouse to act as a pointer input device and send WM_POINTER messages.
old-location: inputmsg\ismouseinpointerenabled.htm
old-project: InputMsg
ms.assetid: 5D493066-2425-4610-8489-575BF25C8C16
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: IsMouseInPointerEnabled, IsMouseInPointerEnabled function [Keyboard and Mouse Input], inputdev.ismouseinpointerenabled, inputmsg.ismouseinpointerenabled, winuser/IsMouseInPointerEnabled
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-L1-1-0.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-L1-1-1.dll
 - MinUser.dll
 - API-Ms-Win-RTCore-NTUser-WMPointer-L1-1-2.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-L1-1-3.dll
api_name:
 - IsMouseInPointerEnabled
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IsMouseInPointerEnabled function


## -description


Indicates whether <a href="https://msdn.microsoft.com/66D9BF17-164F-455F-803F-36CDF88C34FF">EnableMouseInPointer</a> is set for the mouse to  act as a pointer input device and send <a href="https://msdn.microsoft.com/65F4DCD0-DAE1-4AC2-AB36-23D114803138">WM_POINTER</a> messages.


## -parameters






## -returns



If <a href="https://msdn.microsoft.com/66D9BF17-164F-455F-803F-36CDF88C34FF">EnableMouseInPointer</a> is set, the return value is nonzero.

If <a href="https://msdn.microsoft.com/66D9BF17-164F-455F-803F-36CDF88C34FF">EnableMouseInPointer</a> is not set, the return value is zero.




## -remarks




<a href="https://msdn.microsoft.com/66D9BF17-164F-455F-803F-36CDF88C34FF">EnableMouseInPointer</a> can be called only once in the context of a process lifetime.  Prior to the first call, Windows Store apps run with mouse-in-pointer enabled, as do any desktop applications that consume mshtml.dll.  All other desktop applications run with mouse-in-pointer disabled.

On the first call to <a href="https://msdn.microsoft.com/66D9BF17-164F-455F-803F-36CDF88C34FF">EnableMouseInPointer</a> in the process lifetime, the state is changed as specified and the call succeeds.

On subsequent calls to <a href="https://msdn.microsoft.com/66D9BF17-164F-455F-803F-36CDF88C34FF">EnableMouseInPointer</a>, the state will not change.  If the current state is not equal to the specified state, the call fails.

Call <b>IsMouseInPointerEnabled</b> to verify the mouse-in-pointer state.




## -see-also




<a href="https://msdn.microsoft.com/66D9BF17-164F-455F-803F-36CDF88C34FF">EnableMouseInPointer</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/65F4DCD0-DAE1-4AC2-AB36-23D114803138">WM_POINTER</a>
 

 

