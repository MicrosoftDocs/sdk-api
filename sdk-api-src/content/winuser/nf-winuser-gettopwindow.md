---
UID: NF:winuser.GetTopWindow
title: GetTopWindow function (winuser.h)
description: Examines the Z order of the child windows associated with the specified parent window and retrieves a handle to the child window at the top of the Z order.
helpviewer_keywords: ["GetTopWindow","GetTopWindow function [Windows and Messages]","_win32_GetTopWindow","_win32_gettopwindow_cpp","winmsg.gettopwindow","winui._win32_gettopwindow","winuser/GetTopWindow"]
old-location: winmsg\gettopwindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\gettopwindow.htm
ms.date: 12/05/2018
ms.keywords: GetTopWindow, GetTopWindow function [Windows and Messages], _win32_GetTopWindow, _win32_gettopwindow_cpp, winmsg.gettopwindow, winui._win32_gettopwindow, winuser/GetTopWindow
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
 - GetTopWindow
 - winuser/GetTopWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-window-ext-l1-1-1.dll
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
api_name:
 - GetTopWindow
req.apiset: ext-ms-win-ntuser-window-l1-1-4 (introduced in Windows 10, version 10.0.14393)
---

# GetTopWindow function


## -description

Examines the Z order of the child windows associated with the specified parent window and retrieves a handle to the child window at the top of the Z order.

## -parameters

### -param hWnd [in, optional]

Type: <b>HWND</b>

A handle to the parent window whose child windows are to be examined. If this parameter is <b>NULL</b>, the function returns a handle to the window at the top of the Z order.

## -returns

Type: <b>HWND</b>

If the function succeeds, the return value is a handle to the child window at the top of the Z order. If the specified window has no child windows, the return value is <b>NULL</b>. To get extended error information, use the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getnextwindow">GetNextWindow</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getwindow">GetWindow</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/windows">Windows</a>
