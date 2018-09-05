---
UID: NF:winuser.GetProcessWindowStation
title: GetProcessWindowStation function
author: windows-sdk-content
description: Retrieves a handle to the current window station for the calling process.
old-location: winstation\getprocesswindowstation.htm
old-project: winstation
ms.assetid: f8929122-d277-4260-b2a7-5e76eb3ca876
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetProcessWindowStation, GetProcessWindowStation function [Windows Stations and Desktops], _win32_getprocesswindowstation, base.getprocesswindowstation, winstation.getprocesswindowstation, winuser/GetProcessWindowStation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: 
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
 - GetProcessWindowStation
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetProcessWindowStation function


## -description


Retrieves a handle to the current window station for the calling process.


## -parameters






## -returns



If the function succeeds, the return value is a handle to the window station.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The system associates a window station with a process when the process is created. A process can use the 
<a href="https://msdn.microsoft.com/d64814a7-945c-4e73-a977-5f696d60610e">SetProcessWindowStation</a> function to change its window station.

The calling process can use the returned handle in calls to the 
<a href="https://msdn.microsoft.com/64f7361d-1a94-4d5b-86f1-a2a21737668a">GetUserObjectInformation</a>, <a href="https://msdn.microsoft.com/998c2520-7833-4efd-a794-b13b528f0485">GetUserObjectSecurity</a>, 
<a href="https://msdn.microsoft.com/42ce6946-1659-41a3-8ba7-21588583b4bd">SetUserObjectInformation</a>, and <a href="https://msdn.microsoft.com/219e41b8-9ac7-4747-a585-b6b9df6a1c9c">SetUserObjectSecurity</a> functions.

Do not close the handle returned by this function.

A service application is created with an associated window station and desktop, so there is no need to call a USER or GDI function to connect the service to a window station and desktop.




## -see-also




<a href="https://msdn.microsoft.com/51eec935-43c7-495b-b1fc-2bd5ba1e0090">GetThreadDesktop</a>



<a href="https://msdn.microsoft.com/64f7361d-1a94-4d5b-86f1-a2a21737668a">GetUserObjectInformation</a>



<a href="https://msdn.microsoft.com/998c2520-7833-4efd-a794-b13b528f0485">GetUserObjectSecurity</a>



<a href="https://msdn.microsoft.com/d64814a7-945c-4e73-a977-5f696d60610e">SetProcessWindowStation</a>



<a href="https://msdn.microsoft.com/42ce6946-1659-41a3-8ba7-21588583b4bd">SetUserObjectInformation</a>



<a href="https://msdn.microsoft.com/219e41b8-9ac7-4747-a585-b6b9df6a1c9c">SetUserObjectSecurity</a>



<a href="https://msdn.microsoft.com/6214c28f-1035-446c-8c79-5d1dd638af2a">Window Station and Desktop Functions</a>



<a href="https://msdn.microsoft.com/617661e2-3b0d-42a9-9769-2ba0957c31a8">Window Stations</a>
 

 

