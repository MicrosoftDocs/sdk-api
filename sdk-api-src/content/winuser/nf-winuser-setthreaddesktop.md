---
UID: NF:winuser.SetThreadDesktop
title: SetThreadDesktop function (winuser.h)
description: Assigns the specified desktop to the calling thread. All subsequent operations on the desktop use the access rights granted to the desktop.
helpviewer_keywords: ["SetThreadDesktop","SetThreadDesktop function [Windows Stations and Desktops]","_win32_setthreaddesktop","base.setthreaddesktop","winstation.setthreaddesktop","winuser/SetThreadDesktop"]
old-location: winstation\setthreaddesktop.htm
tech.root: winstation
ms.assetid: 619c591f-54b7-4b61-aa07-fc57e05ee37a
ms.date: 12/05/2018
ms.keywords: SetThreadDesktop, SetThreadDesktop function [Windows Stations and Desktops], _win32_setthreaddesktop, base.setthreaddesktop, winstation.setthreaddesktop, winuser/SetThreadDesktop
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
 - SetThreadDesktop
 - winuser/SetThreadDesktop
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-RTCore-NTUser-WindowStation-l1-1-0.dll
 - Ext-MS-Win-NTUser-Windowstation-l1-1-0.dll
 - Ext-MS-Win-NTUser-Windowstation-l1-1-1.dll
 - Ext-MS-Win-NTUser-WindowStation-L1-1-2.dll
api_name:
 - SetThreadDesktop
req.apiset: ext-ms-win-ntuser-windowstation-l1-1-0 (introduced in Windows 8)
---

# SetThreadDesktop function


## -description

Assigns the specified desktop to the calling thread. All subsequent operations on the desktop use the access rights granted to the desktop.

## -parameters

### -param hDesktop [in]

A handle to the desktop to be assigned to the calling thread. This handle is returned by the 
<a href="/windows/desktop/api/winuser/nf-winuser-createdesktopa">CreateDesktop</a>, 
<a href="/windows/desktop/api/winuser/nf-winuser-getthreaddesktop">GetThreadDesktop</a>, <a href="/windows/desktop/api/winuser/nf-winuser-opendesktopa">OpenDesktop</a>, or 
<a href="/windows/desktop/api/winuser/nf-winuser-openinputdesktop">OpenInputDesktop</a> function.

This desktop must be associated with the current window station for the process.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>SetThreadDesktop</b> function will fail if the calling thread has any windows or hooks on its current desktop (unless the <i>hDesktop</i> parameter is a handle to the current desktop).

<div class="alert"><b>Warning</b>  There is a significant security risk for any service that opens a window on the interactive desktop. By opening a desktop window, a service makes itself vulnerable to attack from the logged-on user, whose application could send malicious messages to the service's desktop window and affect its ability to function.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-createdesktopa">CreateDesktop</a>



<a href="/windows/desktop/winstation/desktops">Desktops</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getthreaddesktop">GetThreadDesktop</a>



<a href="/windows/desktop/api/winuser/nf-winuser-opendesktopa">OpenDesktop</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setprocesswindowstation">SetProcessWindowStation</a>



<a href="/windows/desktop/winstation/window-station-and-desktop-functions">Window Station and Desktop Functions</a>
