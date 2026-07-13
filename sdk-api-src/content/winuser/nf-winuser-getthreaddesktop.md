---
UID: NF:winuser.GetThreadDesktop
title: GetThreadDesktop function (winuser.h)
description: Retrieves a handle to the desktop assigned to the specified thread.
helpviewer_keywords: ["GetThreadDesktop","GetThreadDesktop function [Windows Stations and Desktops]","_win32_getthreaddesktop","base.getthreaddesktop","winstation.getthreaddesktop","winuser/GetThreadDesktop"]
old-location: winstation\getthreaddesktop.htm
tech.root: winstation
ms.assetid: 51eec935-43c7-495b-b1fc-2bd5ba1e0090
ms.date: 12/05/2018
ms.keywords: GetThreadDesktop, GetThreadDesktop function [Windows Stations and Desktops], _win32_getthreaddesktop, base.getthreaddesktop, winstation.getthreaddesktop, winuser/GetThreadDesktop
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
 - GetThreadDesktop
 - winuser/GetThreadDesktop
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
 - GetThreadDesktop
req.apiset: ext-ms-win-ntuser-windowstation-l1-1-0 (introduced in Windows 8)
---

# GetThreadDesktop function


## -description

Retrieves a handle to the desktop assigned to the specified thread.

## -parameters

### -param dwThreadId [in]

The thread identifier. The 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid">GetCurrentThreadId</a> and 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> functions return thread identifiers.

## -returns

If the function succeeds, the return value is a handle to the desktop associated with the specified thread. You do not need to call the 
<a href="/windows/desktop/api/winuser/nf-winuser-closedesktop">CloseDesktop</a> function to close the returned handle.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The system associates a desktop with a thread when that thread is created. A thread can use the 
<a href="/windows/desktop/api/winuser/nf-winuser-setthreaddesktop">SetThreadDesktop</a> function to change its desktop. The desktop associated with a thread must be on the window station associated with the thread's process.

The calling process can use the returned handle in calls to the 
<a href="/windows/desktop/api/winuser/nf-winuser-getuserobjectinformationa">GetUserObjectInformation</a>, <a href="/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity">GetUserObjectSecurity</a>, 
<a href="/windows/desktop/api/winuser/nf-winuser-setuserobjectinformationa">SetUserObjectInformation</a>, and <a href="/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity">SetUserObjectSecurity</a> functions.

A service application is created with an associated window station and desktop, so there is no need to call a USER or GDI function to connect the service to a window station and desktop.

## -see-also

<a href="/windows/desktop/winstation/desktops">Desktops</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid">GetCurrentThreadId</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getprocesswindowstation">GetProcessWindowStation</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getuserobjectinformationa">GetUserObjectInformation</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity">GetUserObjectSecurity</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setprocesswindowstation">SetProcessWindowStation</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setthreaddesktop">SetThreadDesktop</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setuserobjectinformationa">SetUserObjectInformation</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity">SetUserObjectSecurity</a>



<a href="/windows/desktop/winstation/window-station-and-desktop-functions">Window Station and Desktop Functions</a>
