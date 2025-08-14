---
UID: NF:winuser.CloseDesktop
title: CloseDesktop function (winuser.h)
description: Closes an open handle to a desktop object.
helpviewer_keywords: ["CloseDesktop","CloseDesktop function [Windows Stations and Desktops]","_win32_closedesktop","base.closedesktop","winstation.closedesktop","winuser/CloseDesktop"]
old-location: winstation\closedesktop.htm
tech.root: winstation
ms.assetid: 861e57b2-061c-4598-ad38-6aef7b79ca54
ms.date: 12/05/2018
ms.keywords: CloseDesktop, CloseDesktop function [Windows Stations and Desktops], _win32_closedesktop, base.closedesktop, winstation.closedesktop, winuser/CloseDesktop
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
 - CloseDesktop
 - winuser/CloseDesktop
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
 - CloseDesktop
req.apiset: ext-ms-win-ntuser-windowstation-l1-1-0 (introduced in Windows 8)
---

# CloseDesktop function


## -description

Closes an open handle to a desktop object.

## -parameters

### -param hDesktop [in]

A handle to the desktop to be closed. This can be a handle returned by the 
<a href="/windows/desktop/api/winuser/nf-winuser-createdesktopa">CreateDesktop</a>, 
<a href="/windows/desktop/api/winuser/nf-winuser-opendesktopa">OpenDesktop</a>, or 
<a href="/windows/desktop/api/winuser/nf-winuser-openinputdesktop">OpenInputDesktop</a> functions. Do not specify the handle returned by the <a href="/windows/desktop/api/winuser/nf-winuser-getthreaddesktop">GetThreadDesktop</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>CloseDesktop</b> function will fail if any thread in the calling process is using the specified desktop handle or if the handle refers to the initial desktop of the calling process.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-createdesktopa">CreateDesktop</a>



<a href="/windows/desktop/winstation/desktops">Desktops</a>



<a href="/windows/desktop/api/winuser/nf-winuser-opendesktopa">OpenDesktop</a>



<a href="/windows/desktop/api/winuser/nf-winuser-openinputdesktop">OpenInputDesktop</a>



<a href="/windows/desktop/winstation/window-station-and-desktop-functions">Window Station and Desktop Functions</a>
