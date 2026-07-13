---
UID: NF:winuser.MoveWindow
title: MoveWindow function (winuser.h)
description: Changes the position and dimensions of the specified window.
helpviewer_keywords: ["MoveWindow","MoveWindow function [Windows and Messages]","_win32_MoveWindow","_win32_movewindow_cpp","winmsg.movewindow","winui._win32_movewindow","winuser/MoveWindow"]
old-location: winmsg\movewindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\movewindow.htm
ms.date: 12/05/2018
ms.keywords: MoveWindow, MoveWindow function [Windows and Messages], _win32_MoveWindow, _win32_movewindow_cpp, winmsg.movewindow, winui._win32_movewindow, winuser/MoveWindow
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
 - MoveWindow
 - winuser/MoveWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-window-l1-1-0.dll
 - ext-ms-win-rtcore-ntuser-window-ext-l1-1-1.dll
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-0.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - MoveWindow
req.apiset: ext-ms-win-ntuser-window-l1-1-1 (introduced in Windows 8.1)
---

# MoveWindow function


## -description

Changes the position and dimensions of the specified window. For a top-level window, the position and dimensions are relative to the upper-left corner of the screen. For a child window, they are relative to the upper-left corner of the parent window's client area.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window.

### -param X [in]

Type: <b>int</b>

The new position of the left side of the window.

### -param Y [in]

Type: <b>int</b>

The new position of the top of the window.

### -param nWidth [in]

Type: <b>int</b>

The new width of the window.

### -param nHeight [in]

Type: <b>int</b>

The new height of the window.

### -param bRepaint [in]

Type: <b>BOOL</b>

Indicates whether the window is to be repainted. If this parameter is <b>TRUE</b>, the window receives a  message. If the parameter is <b>FALSE</b>, no repainting of any kind occurs. This applies to the client area, the nonclient area (including the title bar and scroll bars), and any part of the parent window uncovered as a result of moving a child window.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the <i>bRepaint</i> parameter is <b>TRUE</b>, the system sends the <a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a> message to the window procedure immediately after moving the window (that is, the <b>MoveWindow</b> function calls the <a href="/windows/desktop/api/winuser/nf-winuser-updatewindow">UpdateWindow</a> function). If <i>bRepaint</i> is <b>FALSE</b>, the application must explicitly invalidate or redraw any parts of the window and parent window that need redrawing.

<b>MoveWindow</b> sends the <a href="/windows/desktop/winmsg/wm-windowposchanging">WM_WINDOWPOSCHANGING</a>, <a href="/windows/desktop/winmsg/wm-windowposchanged">WM_WINDOWPOSCHANGED</a>, <a href="/windows/desktop/winmsg/wm-move">WM_MOVE</a>, <a href="/windows/desktop/winmsg/wm-size">WM_SIZE</a>, and <a href="/windows/desktop/winmsg/wm-nccalcsize">WM_NCCALCSIZE</a> messages to the window. 


#### Examples

For an example, see <a href="/windows/desktop/winmsg/using-windows">Creating, Enumerating, and Sizing Child Windows</a>.

<div class="code"></div>

## -see-also

<b>Conceptual</b>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowpos">SetWindowPos</a>



<a href="/windows/desktop/api/winuser/nf-winuser-updatewindow">UpdateWindow</a>



<a href="/windows/desktop/winmsg/wm-getminmaxinfo">WM_GETMINMAXINFO</a>



<a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
