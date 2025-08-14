---
UID: NF:winuser.SetProcessWindowStation
title: SetProcessWindowStation function (winuser.h)
description: Assigns the specified window station to the calling process.
helpviewer_keywords: ["SetProcessWindowStation","SetProcessWindowStation function [Windows Stations and Desktops]","_win32_setprocesswindowstation","base.setprocesswindowstation","winstation.setprocesswindowstation","winuser/SetProcessWindowStation"]
old-location: winstation\setprocesswindowstation.htm
tech.root: winstation
ms.assetid: d64814a7-945c-4e73-a977-5f696d60610e
ms.date: 12/05/2018
ms.keywords: SetProcessWindowStation, SetProcessWindowStation function [Windows Stations and Desktops], _win32_setprocesswindowstation, base.setprocesswindowstation, winstation.setprocesswindowstation, winuser/SetProcessWindowStation
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
 - SetProcessWindowStation
 - winuser/SetProcessWindowStation
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
 - API-MS-Win-RTCore-NTUser-WindowStation-l1-1-0.dll
 - Ext-MS-Win-NTUser-Windowstation-l1-1-0.dll
 - Ext-MS-Win-NTUser-Windowstation-l1-1-1.dll
 - Ext-MS-Win-NTUser-WindowStation-L1-1-2.dll
api_name:
 - SetProcessWindowStation
req.apiset: ext-ms-win-ntuser-windowstation-l1-1-0 (introduced in Windows 8)
---

# SetProcessWindowStation function


## -description

Assigns the specified window station to the calling process. This enables the process to access objects in the window station such as desktops, the clipboard, and global atoms. All subsequent operations on the window station use the access rights granted to <i>hWinSta</i>.

## -parameters

### -param hWinSta [in]

A handle to the window station. This can be a handle returned by the 
<a href="/windows/desktop/api/winuser/nf-winuser-createwindowstationa">CreateWindowStation</a>, 
<a href="/windows/desktop/api/winuser/nf-winuser-openwindowstationa">OpenWindowStation</a>, or 
<a href="/windows/desktop/api/winuser/nf-winuser-getprocesswindowstation">GetProcessWindowStation</a> function.

This window station must be associated with the current session.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-createwindowstationa">CreateWindowStation</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getprocesswindowstation">GetProcessWindowStation</a>



<a href="/windows/desktop/api/winuser/nf-winuser-openwindowstationa">OpenWindowStation</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setthreaddesktop">SetThreadDesktop</a>



<a href="/windows/desktop/winstation/window-station-and-desktop-functions">Window Station and Desktop Functions</a>



<a href="/windows/desktop/winstation/window-stations">Window Stations</a>
