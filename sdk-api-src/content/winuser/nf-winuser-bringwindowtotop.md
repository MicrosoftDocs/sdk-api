---
UID: NF:winuser.BringWindowToTop
title: BringWindowToTop function (winuser.h)
description: Brings the specified window to the top of the Z order. If the window is a top-level window, it is activated. If the window is a child window, the top-level parent window associated with the child window is activated.
helpviewer_keywords: ["BringWindowToTop","BringWindowToTop function [Windows and Messages]","_win32_BringWindowToTop","_win32_bringwindowtotop_cpp","winmsg.bringwindowtotop","winui._win32_bringwindowtotop","winuser/BringWindowToTop"]
old-location: winmsg\bringwindowtotop.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\bringwindowtotop.htm
ms.date: 12/05/2018
ms.keywords: BringWindowToTop, BringWindowToTop function [Windows and Messages], _win32_BringWindowToTop, _win32_bringwindowtotop_cpp, winmsg.bringwindowtotop, winui._win32_bringwindowtotop, winuser/BringWindowToTop
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
 - BringWindowToTop
 - winuser/BringWindowToTop
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
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - BringWindowToTop
req.apiset: ext-ms-win-ntuser-window-l1-1-0 (introduced in Windows 8)
---

# BringWindowToTop function


## -description

Brings the specified window to the top of the Z order. If the window is a top-level window, it is activated. If the window is a child window, the top-level parent window associated with the child window is activated.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window to bring to the top of the Z order.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Use the <b>BringWindowToTop</b> function to uncover any window that is partially or completely obscured by other windows. 

Calling this function is similar to calling the <a href="/windows/desktop/api/winuser/nf-winuser-setwindowpos">SetWindowPos</a> function to change a window's position in the Z order. <b>BringWindowToTop</b> does not make a window a top-level window.

## -see-also

<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowpos">SetWindowPos</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
