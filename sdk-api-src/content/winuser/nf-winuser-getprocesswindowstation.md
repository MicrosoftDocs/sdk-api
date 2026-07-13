---
UID: NF:winuser.GetProcessWindowStation
title: GetProcessWindowStation function (winuser.h)
description: Retrieves a handle to the current window station for the calling process.
helpviewer_keywords: ["GetProcessWindowStation","GetProcessWindowStation function [Windows Stations and Desktops]","_win32_getprocesswindowstation","base.getprocesswindowstation","winstation.getprocesswindowstation","winuser/GetProcessWindowStation"]
old-location: winstation\getprocesswindowstation.htm
tech.root: winstation
ms.assetid: f8929122-d277-4260-b2a7-5e76eb3ca876
ms.date: 12/05/2018
ms.keywords: GetProcessWindowStation, GetProcessWindowStation function [Windows Stations and Desktops], _win32_getprocesswindowstation, base.getprocesswindowstation, winstation.getprocesswindowstation, winuser/GetProcessWindowStation
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetProcessWindowStation
 - winuser/GetProcessWindowStation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-winstamin-l1-1-0.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Windowstation-l1-1-0.dll
 - Ext-MS-Win-NTUser-Windowstation-l1-1-1.dll
 - api-ms-win-rtcore-ntuser-windowstation-l1-1-0.dll
 - Ext-MS-Win-NTUser-WindowStation-L1-1-2.dll
api_name:
 - GetProcessWindowStation
req.apiset: ext-ms-win-ntuser-windowstation-l1-1-0 (introduced in Windows 8)
---

# GetProcessWindowStation function


## -description

Retrieves a handle to the current window station for the calling process.



## -returns

If the function succeeds, the return value is a handle to the window station.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The system associates a window station with a process when the process is created. A process can use the 
<a href="/windows/desktop/api/winuser/nf-winuser-setprocesswindowstation">SetProcessWindowStation</a> function to change its window station.

The calling process can use the returned handle in calls to the 
<a href="/windows/desktop/api/winuser/nf-winuser-getuserobjectinformationa">GetUserObjectInformation</a>, <a href="/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity">GetUserObjectSecurity</a>, 
<a href="/windows/desktop/api/winuser/nf-winuser-setuserobjectinformationa">SetUserObjectInformation</a>, and <a href="/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity">SetUserObjectSecurity</a> functions.

Do not close the handle returned by this function.

A service application is created with an associated window station and desktop, so there is no need to call a USER or GDI function to connect the service to a window station and desktop.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-getthreaddesktop">GetThreadDesktop</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getuserobjectinformationa">GetUserObjectInformation</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity">GetUserObjectSecurity</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setprocesswindowstation">SetProcessWindowStation</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setuserobjectinformationa">SetUserObjectInformation</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity">SetUserObjectSecurity</a>



<a href="/windows/desktop/winstation/window-station-and-desktop-functions">Window Station and Desktop Functions</a>



<a href="/windows/desktop/winstation/window-stations">Window Stations</a>
