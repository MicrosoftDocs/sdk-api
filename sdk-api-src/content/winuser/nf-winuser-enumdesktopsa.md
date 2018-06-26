---
UID: NF:winuser.EnumDesktopsA
title: EnumDesktopsA function
author: windows-sdk-content
description: Enumerates all desktops associated with the specified window station of the calling process. The function passes the name of each desktop, in turn, to an application-defined callback function.
old-location: winstation\enumdesktops.htm
old-project: winstation
ms.assetid: 3e900b34-2c60-4281-881f-13a746674aec
ms.author: windowssdkdev
ms.date: 03/26/2018
ms.keywords: EnumDesktops, EnumDesktops function [Windows Stations and Desktops], EnumDesktopsA, EnumDesktopsW, _win32_enumdesktops, base.enumdesktops, winstation.enumdesktops, winuser/EnumDesktops, winuser/EnumDesktopsA, winuser/EnumDesktopsW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumDesktopsW (Unicode) and EnumDesktopsA (ANSI)
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
 - EnumDesktops
 - EnumDesktopsA
 - EnumDesktopsW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# EnumDesktopsA function


## -description


Enumerates all desktops associated with the specified window station of the calling process. The function passes the name of each desktop, in turn, to an application-defined callback function.


## -parameters




### -param hwinsta [in, optional]

A handle to the window station whose desktops are to be enumerated. This handle is returned by the 
<a href="https://msdn.microsoft.com/c1aee546-decd-46c9-8d02-d6792f5a6a0d">CreateWindowStation</a>, 
<a href="https://msdn.microsoft.com/f8929122-d277-4260-b2a7-5e76eb3ca876">GetProcessWindowStation</a>, or 
<a href="https://msdn.microsoft.com/78ee7100-1bad-4c2d-b923-c5e67191bd41">OpenWindowStation</a> function, and must have the WINSTA_ENUMDESKTOPS access right. For more information, see 
<a href="https://msdn.microsoft.com/b132da61-26b7-4457-9433-4894ca0e640a">Window Station Security and Access Rights</a>.

If this parameter is NULL, the current window station is used.


### -param lpEnumFunc [in]

A pointer to an application-defined 
<a href="https://msdn.microsoft.com/0f02db91-2ce3-44ee-a116-1bea693b2739">EnumDesktopProc</a> callback function.


### -param lParam [in]

An application-defined value to be passed to the callback function.


## -returns



If the function succeeds, it returns the  nonzero value returned by the callback function that was pointed to by <i>lpEnumFunc</i>.

If the function is unable to perform the enumeration, the return value is zero. Call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to get extended error information.

If the callback function fails, the return value is zero. The callback function can  call <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> to set an error code for the caller to retrieve by calling <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>EnumDesktops</b> function enumerates only those desktops for which the calling process has the DESKTOP_ENUMERATE access right. For more information, see 
<a href="https://msdn.microsoft.com/6512d128-3b0c-4ba7-8709-2fd225389a40">Desktop Security and Access Rights</a>.

The 
<b>EnumDesktops</b> function repeatedly invokes the <i>lpEnumFunc</i> callback function until the last desktop is enumerated or the callback function returns FALSE.




## -see-also




<a href="https://msdn.microsoft.com/c1aee546-decd-46c9-8d02-d6792f5a6a0d">CreateWindowStation</a>



<a href="https://msdn.microsoft.com/c56cd63b-c260-40d0-9a62-1dee1eb18679">Desktops</a>



<a href="https://msdn.microsoft.com/0f02db91-2ce3-44ee-a116-1bea693b2739">EnumDesktopProc</a>



<a href="https://msdn.microsoft.com/f8929122-d277-4260-b2a7-5e76eb3ca876">GetProcessWindowStation</a>



<a href="https://msdn.microsoft.com/78ee7100-1bad-4c2d-b923-c5e67191bd41">OpenWindowStation</a>



<a href="https://msdn.microsoft.com/6214c28f-1035-446c-8c79-5d1dd638af2a">Window Station and Desktop Functions</a>
 

 

