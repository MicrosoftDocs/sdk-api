---
UID: NF:winuser.SwitchDesktop
title: SwitchDesktop function (winuser.h)
author: windows-sdk-content
description: Makes the specified desktop visible and activates it. This enables the desktop to receive input from the user.
old-location: winstation\switchdesktop.htm
tech.root: winstation
ms.assetid: 401be515-ada9-42be-b8e8-4e86f513bb8d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SwitchDesktop, SwitchDesktop function [Windows Stations and Desktops], base.switchdesktop, winstation.switchdesktop, winuser/SwitchDesktop
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
 - Ext-MS-Win-NTUser-Windowstation-l1-1-0.dll
 - Ext-MS-Win-NTUser-Windowstation-l1-1-1.dll
 - api-ms-win-rtcore-ntuser-windowstation-l1-1-0.dll
 - Ext-MS-Win-NTUser-WindowStation-L1-1-2.dll
api_name:
 - SwitchDesktop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SwitchDesktop function


## -description


Makes the specified desktop visible and activates it. This enables the desktop to receive input from the user. The calling process must have DESKTOP_SWITCHDESKTOP access to the desktop for the 
<b>SwitchDesktop</b> function to succeed.


## -parameters




### -param hDesktop [in]

A handle to the desktop. This handle is returned by the 
<a href="https://msdn.microsoft.com/c6ed40c5-13a9-4697-a727-730adc6a912d">CreateDesktop</a> and 
<a href="https://msdn.microsoft.com/7f805f47-1737-4f4b-a74a-9c1423b65f2c">OpenDesktop</a> functions.

This desktop must be associated with the current window station for the process.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. However, 
<b>SwitchDesktop</b> only sets the last error for the following cases:

<ul>
<li>When the desktop belongs to an invisible window station</li>
<li>When <i>hDesktop</i> is an invalid handle, refers to a destroyed desktop, or belongs to a different session than that of the calling process</li>
</ul>



## -remarks



The 
<b>SwitchDesktop</b> function fails if the desktop belongs to an invisible window station. 
<b>SwitchDesktop</b> also fails when called from a process that is associated with a secured desktop such as the WinLogon and ScreenSaver desktops. Processes that are associated with a secured desktop include custom UserInit processes. Such calls typically fail with an "access denied" error.




## -see-also




<a href="https://msdn.microsoft.com/c6ed40c5-13a9-4697-a727-730adc6a912d">CreateDesktop</a>



<a href="https://msdn.microsoft.com/c56cd63b-c260-40d0-9a62-1dee1eb18679">Desktops</a>



<a href="https://msdn.microsoft.com/7f805f47-1737-4f4b-a74a-9c1423b65f2c">OpenDesktop</a>



<a href="https://msdn.microsoft.com/6214c28f-1035-446c-8c79-5d1dd638af2a">Window Station and Desktop Functions</a>
 

 

