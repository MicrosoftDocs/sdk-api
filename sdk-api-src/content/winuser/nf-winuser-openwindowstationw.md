---
UID: NF:winuser.OpenWindowStationW
title: OpenWindowStationW function
author: windows-sdk-content
description: Opens the specified window station.
old-location: winstation\openwindowstation.htm
old-project: winstation
ms.assetid: 78ee7100-1bad-4c2d-b923-c5e67191bd41
ms.author: windowssdkdev
ms.date: 03/27/2018
ms.keywords: OpenWindowStation, OpenWindowStation function [Windows Stations and Desktops], OpenWindowStationA, OpenWindowStationW, _win32_openwindowstation, base.openwindowstation, winstation.openwindowstation, winuser/OpenWindowStation, winuser/OpenWindowStationA, winuser/OpenWindowStationW
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
req.unicode-ansi: OpenWindowStationW (Unicode) and OpenWindowStationA (ANSI)
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
 - API-MS-Win-RTCore-NTUser-WindowStation-l1-1-0.dll
 - Ext-MS-Win-NTUser-WindowStation-Ansi-L1-1-1.dll
 - Ext-MS-Win-NTUser-Windowstation-L1-1-0.dll
 - Ext-MS-Win-NTUser-Windowstation-L1-1-1.dll
 - Ext-MS-Win-NTUser-WindowStation-L1-1-2.dll
api_name:
 - OpenWindowStation
 - OpenWindowStationA
 - OpenWindowStationW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# OpenWindowStationW function


## -description


Opens the specified window station.


## -parameters




### -param lpszWinSta [in]

The name of the window station to be opened. Window station names are case-insensitive.

This window station must belong to the current session.


### -param fInherit [in]

If this value is <b>TRUE</b>, processes created by this process will inherit the handle. Otherwise, the processes do not inherit this handle.


### -param dwDesiredAccess [in]

The access to the window station. For a list of access rights, see 
<a href="https://msdn.microsoft.com/b132da61-26b7-4457-9433-4894ca0e640a">Window Station Security and Access Rights</a>.


## -returns



If the function succeeds, the return value is the handle to the specified window station.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



After you are done with the handle, you must call 
<a href="https://msdn.microsoft.com/417cb01b-c206-4b5b-9516-94e5d90717f4">CloseWindowStation</a> to free the handle.




## -see-also




<a href="https://msdn.microsoft.com/417cb01b-c206-4b5b-9516-94e5d90717f4">CloseWindowStation</a>



<a href="https://msdn.microsoft.com/7c76caac-459d-45df-ae00-bc208a9e7b22">ExitWindows</a>



<a href="https://msdn.microsoft.com/f44ccb66-10bd-4ee6-93e1-16948cf10e50">ExitWindowsEx</a>



<a href="https://msdn.microsoft.com/6214c28f-1035-446c-8c79-5d1dd638af2a">Window Station and Desktop Functions</a>



<a href="https://msdn.microsoft.com/617661e2-3b0d-42a9-9769-2ba0957c31a8">Window Stations</a>
 

 

