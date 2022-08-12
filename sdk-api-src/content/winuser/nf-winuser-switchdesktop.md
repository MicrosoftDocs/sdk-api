---
UID: NF:winuser.SwitchDesktop
title: SwitchDesktop function (winuser.h)
description: Makes the specified desktop visible and activates it. This enables the desktop to receive input from the user.
helpviewer_keywords: ["SwitchDesktop","SwitchDesktop function [Windows Stations and Desktops]","base.switchdesktop","winstation.switchdesktop","winuser/SwitchDesktop"]
old-location: winstation\switchdesktop.htm
tech.root: winstation
ms.assetid: 401be515-ada9-42be-b8e8-4e86f513bb8d
ms.date: 12/05/2018
ms.keywords: SwitchDesktop, SwitchDesktop function [Windows Stations and Desktops], base.switchdesktop, winstation.switchdesktop, winuser/SwitchDesktop
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
 - SwitchDesktop
 - winuser/SwitchDesktop
dev_langs:
 - c++
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
req.apiset: ext-ms-win-ntuser-windowstation-l1-1-0 (introduced in Windows 8)
---

# SwitchDesktop function


## -description

Makes the specified desktop visible and activates it. This enables the desktop to receive input from the user. The calling process must have DESKTOP_SWITCHDESKTOP access to the desktop for the 
<b>SwitchDesktop</b> function to succeed.

## -parameters

### -param hDesktop [in]

A handle to the desktop. This handle is returned by the 
<a href="/windows/desktop/api/winuser/nf-winuser-createdesktopa">CreateDesktop</a> and 
<a href="/windows/desktop/api/winuser/nf-winuser-opendesktopa">OpenDesktop</a> functions.

This desktop must be associated with the current window station for the process.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. However, 
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

<a href="/windows/desktop/api/winuser/nf-winuser-createdesktopa">CreateDesktop</a>



<a href="/windows/desktop/winstation/desktops">Desktops</a>



<a href="/windows/desktop/api/winuser/nf-winuser-opendesktopa">OpenDesktop</a>



<a href="/windows/desktop/winstation/window-station-and-desktop-functions">Window Station and Desktop Functions</a>
