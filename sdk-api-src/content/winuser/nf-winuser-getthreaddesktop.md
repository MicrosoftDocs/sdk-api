---
UID: NF:winuser.GetThreadDesktop
title: GetThreadDesktop function (winuser.h)
author: windows-sdk-content
description: Retrieves a handle to the desktop assigned to the specified thread.
old-location: winstation\getthreaddesktop.htm
tech.root: winstation
ms.assetid: 51eec935-43c7-495b-b1fc-2bd5ba1e0090
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetThreadDesktop, GetThreadDesktop function [Windows Stations and Desktops], _win32_getthreaddesktop, base.getthreaddesktop, winstation.getthreaddesktop, winuser/GetThreadDesktop
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
 - GetThreadDesktop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetThreadDesktop function


## -description


Retrieves a handle to the desktop assigned to the specified thread.


## -parameters




### -param dwThreadId [in]

The thread identifier. The 
<a href="https://msdn.microsoft.com/a496f61a-e027-44e7-8b22-4f6651d7afb2">GetCurrentThreadId</a> and 
<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a> functions return thread identifiers.


## -returns



If the function succeeds, the return value is a handle to the desktop associated with the specified thread. You do not need to call the 
<a href="https://msdn.microsoft.com/861e57b2-061c-4598-ad38-6aef7b79ca54">CloseDesktop</a> function to close the returned handle.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The system associates a desktop with a thread when that thread is created. A thread can use the 
<a href="https://msdn.microsoft.com/619c591f-54b7-4b61-aa07-fc57e05ee37a">SetThreadDesktop</a> function to change its desktop. The desktop associated with a thread must be on the window station associated with the thread's process.

The calling process can use the returned handle in calls to the 
<a href="https://msdn.microsoft.com/64f7361d-1a94-4d5b-86f1-a2a21737668a">GetUserObjectInformation</a>, <a href="https://msdn.microsoft.com/998c2520-7833-4efd-a794-b13b528f0485">GetUserObjectSecurity</a>, 
<a href="https://msdn.microsoft.com/42ce6946-1659-41a3-8ba7-21588583b4bd">SetUserObjectInformation</a>, and <a href="https://msdn.microsoft.com/219e41b8-9ac7-4747-a585-b6b9df6a1c9c">SetUserObjectSecurity</a> functions.

A service application is created with an associated window station and desktop, so there is no need to call a USER or GDI function to connect the service to a window station and desktop.




## -see-also




<a href="https://msdn.microsoft.com/c56cd63b-c260-40d0-9a62-1dee1eb18679">Desktops</a>



<a href="https://msdn.microsoft.com/a496f61a-e027-44e7-8b22-4f6651d7afb2">GetCurrentThreadId</a>



<a href="https://msdn.microsoft.com/f8929122-d277-4260-b2a7-5e76eb3ca876">GetProcessWindowStation</a>



<a href="https://msdn.microsoft.com/64f7361d-1a94-4d5b-86f1-a2a21737668a">GetUserObjectInformation</a>



<a href="https://msdn.microsoft.com/998c2520-7833-4efd-a794-b13b528f0485">GetUserObjectSecurity</a>



<a href="https://msdn.microsoft.com/d64814a7-945c-4e73-a977-5f696d60610e">SetProcessWindowStation</a>



<a href="https://msdn.microsoft.com/619c591f-54b7-4b61-aa07-fc57e05ee37a">SetThreadDesktop</a>



<a href="https://msdn.microsoft.com/42ce6946-1659-41a3-8ba7-21588583b4bd">SetUserObjectInformation</a>



<a href="https://msdn.microsoft.com/219e41b8-9ac7-4747-a585-b6b9df6a1c9c">SetUserObjectSecurity</a>



<a href="https://msdn.microsoft.com/6214c28f-1035-446c-8c79-5d1dd638af2a">Window Station and Desktop Functions</a>
 

 

