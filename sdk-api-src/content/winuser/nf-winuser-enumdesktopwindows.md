---
UID: NF:winuser.EnumDesktopWindows
title: EnumDesktopWindows function (winuser.h)
description: Enumerates all top-level windows associated with the specified desktop. It passes the handle to each window, in turn, to an application-defined callback function.
helpviewer_keywords: ["EnumDesktopWindows","EnumDesktopWindows function [Windows Stations and Desktops]","_win32_enumdesktopwindows","base.enumdesktopwindows","winstation.enumdesktopwindows","winuser/EnumDesktopWindows"]
old-location: winstation\enumdesktopwindows.htm
tech.root: winstation
ms.assetid: b399ff19-e2e5-4509-8bb5-9647734881b3
ms.date: 12/05/2018
ms.keywords: EnumDesktopWindows, EnumDesktopWindows function [Windows Stations and Desktops], _win32_enumdesktopwindows, base.enumdesktopwindows, winstation.enumdesktopwindows, winuser/EnumDesktopWindows
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
 - EnumDesktopWindows
 - winuser/EnumDesktopWindows
dev_langs:
 - c++
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
req.apiset: ext-ms-win-ntuser-windowstation-l1-1-0 (introduced in Windows 8)
---

# EnumDesktopWindows function


## -description

Enumerates all top-level windows associated with the specified desktop. It passes the handle to each window, in turn, to an application-defined callback function.

## -parameters

### -param hDesktop [in, optional]

A handle to the desktop whose top-level windows are to be enumerated. This handle is returned by the 
<a href="/windows/desktop/api/winuser/nf-winuser-createdesktopa">CreateDesktop</a>, 
<a href="/windows/desktop/api/winuser/nf-winuser-getthreaddesktop">GetThreadDesktop</a>, <a href="/windows/desktop/api/winuser/nf-winuser-opendesktopa">OpenDesktop</a>, or 
<a href="/windows/desktop/api/winuser/nf-winuser-openinputdesktop">OpenInputDesktop</a> function, and must have the <b>DESKTOP_READOBJECTS</b> access right. For more information, see 
<a href="/windows/desktop/winstation/desktop-security-and-access-rights">Desktop Security and Access Rights</a>.

If this parameter is NULL, the current desktop is used.

### -param lpfn [in]

A pointer to an application-defined 
<a href="/previous-versions/windows/desktop/legacy/ms633498(v=vs.85)">EnumWindowsProc</a> callback function.

### -param lParam [in]

An application-defined value to be passed to the callback function.

## -returns

If the function fails or is unable to perform the enumeration, the return value is zero.

To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

You must ensure that the callback function sets <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> if it fails.

<b>Windows Server 2003 and Windows XP/2000:  </b>If there are no windows on the desktop, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_INVALID_HANDLE</b>.

## -remarks

The 
<b>EnumDesktopWindows</b> function repeatedly invokes the <i>lpfn</i> callback function until the last top-level window is enumerated or the callback function returns <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-createdesktopa">CreateDesktop</a>



<a href="/windows/desktop/winstation/desktops">Desktops</a>



<a href="/previous-versions/windows/desktop/legacy/ms633498(v=vs.85)">EnumWindowsProc</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getthreaddesktop">GetThreadDesktop</a>



<a href="/windows/desktop/api/winuser/nf-winuser-opendesktopa">OpenDesktop</a>



<a href="/windows/desktop/winstation/window-station-and-desktop-functions">Window Station and Desktop Functions</a>
