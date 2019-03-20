---
UID: NF:winuser.EnumDesktopWindows
title: EnumDesktopWindows function (winuser.h)
author: windows-sdk-content
description: Enumerates all top-level windows associated with the specified desktop. It passes the handle to each window, in turn, to an application-defined callback function.
old-location: winstation\enumdesktopwindows.htm
tech.root: winstation
ms.assetid: b399ff19-e2e5-4509-8bb5-9647734881b3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EnumDesktopWindows, EnumDesktopWindows function [Windows Stations and Desktops], _win32_enumdesktopwindows, base.enumdesktopwindows, winstation.enumdesktopwindows, winuser/EnumDesktopWindows
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - API-MS-Win-RTCore-NTUser-WindowStation-L1-1-0.dll
 - Ext-MS-Win-NTUser-Windowstation-L1-1-0.dll
 - Ext-MS-Win-NTUser-Windowstation-L1-1-1.dll
 - Ext-MS-Win-NTUser-WindowStation-L1-1-2.dll
api_name:
 - EnumDesktopWindows
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EnumDesktopWindows function


## -description


Enumerates all top-level windows associated with the specified desktop. It passes the handle to each window, in turn, to an application-defined callback function.


## -parameters




### -param hDesktop [in, optional]

A handle to the desktop whose top-level windows are to be enumerated. This handle is returned by the 
<a href="https://msdn.microsoft.com/c6ed40c5-13a9-4697-a727-730adc6a912d">CreateDesktop</a>, 
<a href="https://msdn.microsoft.com/51eec935-43c7-495b-b1fc-2bd5ba1e0090">GetThreadDesktop</a>, <a href="https://msdn.microsoft.com/7f805f47-1737-4f4b-a74a-9c1423b65f2c">OpenDesktop</a>, or 
<a href="https://msdn.microsoft.com/023d421e-bf32-4e08-b5b3-b7b2ca6c4e00">OpenInputDesktop</a> function, and must have the <b>DESKTOP_READOBJECTS</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/6512d128-3b0c-4ba7-8709-2fd225389a40">Desktop Security and Access Rights</a>.

If this parameter is NULL, the current desktop is used.


### -param lpfn [in]

A pointer to an application-defined 
<a href="https://msdn.microsoft.com/en-us/library/ms633498(v=VS.85).aspx">EnumWindowsProc</a> callback function.


### -param lParam [in]

An application-defined value to be passed to the callback function.


## -returns



If the function fails or is unable to perform the enumeration, the return value is zero.

To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

You must ensure that the callback function sets <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> if it fails.

<b>Windows Server 2003 and Windows XP/2000:  </b>If there are no windows on the desktop, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_INVALID_HANDLE</b>.




## -remarks



The 
<b>EnumDesktopWindows</b> function repeatedly invokes the <i>lpfn</i> callback function until the last top-level window is enumerated or the callback function returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/c6ed40c5-13a9-4697-a727-730adc6a912d">CreateDesktop</a>



<a href="https://msdn.microsoft.com/c56cd63b-c260-40d0-9a62-1dee1eb18679">Desktops</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633498(v=VS.85).aspx">EnumWindowsProc</a>



<a href="https://msdn.microsoft.com/51eec935-43c7-495b-b1fc-2bd5ba1e0090">GetThreadDesktop</a>



<a href="https://msdn.microsoft.com/7f805f47-1737-4f4b-a74a-9c1423b65f2c">OpenDesktop</a>



<a href="https://msdn.microsoft.com/6214c28f-1035-446c-8c79-5d1dd638af2a">Window Station and Desktop Functions</a>
 

 

