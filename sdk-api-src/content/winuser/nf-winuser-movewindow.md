---
UID: NF:winuser.MoveWindow
title: MoveWindow function
author: windows-sdk-content
description: Changes the position and dimensions of the specified window.
old-location: winmsg\movewindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\movewindow.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: MoveWindow, MoveWindow function [Windows and Messages], _win32_MoveWindow, _win32_movewindow_cpp, winmsg.movewindow, winui._win32_movewindow, winuser/MoveWindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the <i>bRepaint</i> parameter is <b>TRUE</b>, the system sends the <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a> message to the window procedure immediately after moving the window (that is, the <b>MoveWindow</b> function calls the <a href="https://msdn.microsoft.com/51a50f1f-7b4d-4acd-83a0-1877f5181766">UpdateWindow</a> function). If <i>bRepaint</i> is <b>FALSE</b>, the application must explicitly invalidate or redraw any parts of the window and parent window that need redrawing.

<b>MoveWindow</b> sends the <a href="https://msdn.microsoft.com/45ecd966-5222-4738-9e99-8a6edbdd435a">WM_WINDOWPOSCHANGING</a>, <a href="https://msdn.microsoft.com/1eabd0b1-1f92-4576-b7fb-8af50fb04526">WM_WINDOWPOSCHANGED</a>, <a href="https://msdn.microsoft.com/552ddc26-fe63-449b-8c82-bb927a2c1c41">WM_MOVE</a>, <a href="https://msdn.microsoft.com/e3e14dcd-9236-48bd-a692-6985d8146f81">WM_SIZE</a>, and <a href="https://msdn.microsoft.com/d2d5825e-02a5-44b8-8615-55b7259d24ba">WM_NCCALCSIZE</a> messages to the window. 


#### Examples

For an example, see <a href="using_windows.htm">Creating, Enumerating, and Sizing Child Windows</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/e0a28590-0fed-4ffa-adcd-84b60df316b5">SetWindowPos</a>



<a href="https://msdn.microsoft.com/51a50f1f-7b4d-4acd-83a0-1877f5181766">UpdateWindow</a>



<a href="https://msdn.microsoft.com/af2295e0-2d0b-4ac0-b689-16138022f4b7">WM_GETMINMAXINFO</a>



<a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a>



<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows</a>
 

 

