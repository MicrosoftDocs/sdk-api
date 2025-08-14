---
UID: NF:winuser.GetTitleBarInfo
title: GetTitleBarInfo function (winuser.h)
description: Retrieves information about the specified title bar.
helpviewer_keywords: ["GetTitleBarInfo","GetTitleBarInfo function [Windows and Messages]","_win32_GetTitleBarInfo","_win32_gettitlebarinfo_cpp","winmsg.gettitlebarinfo","winui._win32_gettitlebarinfo","winuser/GetTitleBarInfo"]
old-location: winmsg\gettitlebarinfo.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\gettitlebarinfo.htm
ms.date: 12/05/2018
ms.keywords: GetTitleBarInfo, GetTitleBarInfo function [Windows and Messages], _win32_GetTitleBarInfo, _win32_gettitlebarinfo_cpp, winmsg.gettitlebarinfo, winui._win32_gettitlebarinfo, winuser/GetTitleBarInfo
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
 - GetTitleBarInfo
 - winuser/GetTitleBarInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetTitleBarInfo
req.apiset: ext-ms-win-ntuser-window-l1-1-3 (introduced in Windows 10, version 10.0.10240)
---

# GetTitleBarInfo function


## -description

Retrieves information about the specified title bar.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

A handle to the title bar whose information is to be retrieved.

### -param pti [in, out]

Type: <b>PTITLEBARINFO</b>

A pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-titlebarinfo">TITLEBARINFO</a> structure to receive the information. Note that you must set the <b>cbSize</b> member to <code>sizeof(TITLEBARINFO)</code> before calling this function.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/ns-winuser-titlebarinfo">TITLEBARINFO</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
