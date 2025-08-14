---
UID: NF:winuser.CloseWindowStation
title: CloseWindowStation function (winuser.h)
description: Closes an open window station handle.
helpviewer_keywords: ["CloseWindowStation","CloseWindowStation function [Windows Stations and Desktops]","_win32_closewindowstation","base.closewindowstation","winstation.closewindowstation","winuser/CloseWindowStation"]
old-location: winstation\closewindowstation.htm
tech.root: winstation
ms.assetid: 417cb01b-c206-4b5b-9516-94e5d90717f4
ms.date: 12/05/2018
ms.keywords: CloseWindowStation, CloseWindowStation function [Windows Stations and Desktops], _win32_closewindowstation, base.closewindowstation, winstation.closewindowstation, winuser/CloseWindowStation
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
 - CloseWindowStation
 - winuser/CloseWindowStation
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
 - CloseWindowStation
req.apiset: ext-ms-win-ntuser-windowstation-l1-1-0 (introduced in Windows 8)
---

# CloseWindowStation function


## -description

Closes an open window station handle.

## -parameters

### -param hWinSta [in]

A handle to the window station to be closed. This handle is returned by the 
<a href="/windows/desktop/api/winuser/nf-winuser-createwindowstationa">CreateWindowStation</a> or 
<a href="/windows/desktop/api/winuser/nf-winuser-openwindowstationa">OpenWindowStation</a> function. Do not specify the handle returned by the <a href="/windows/desktop/api/winuser/nf-winuser-getprocesswindowstation">GetProcessWindowStation</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<b>Windows Server 2003 and Windows XP/2000:  </b>This function does not set the last error code on failure.

## -remarks

The 
<b>CloseWindowStation</b> function will fail if the handle being closed is for the window station assigned to the calling process.

## -see-also

<a href="/windows/desktop/winstation/window-station-and-desktop-functions">Window Station and Desktop Functions</a>



<a href="/windows/desktop/winstation/window-stations">Window Stations</a>
