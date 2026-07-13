---
UID: NF:winuser.SetActiveWindow
title: SetActiveWindow function (winuser.h)
description: Activates a window. The window must be attached to the calling thread's message queue.
helpviewer_keywords: ["SetActiveWindow","SetActiveWindow function [Keyboard and Mouse Input]","_win32_SetActiveWindow","_win32_setactivewindow_cpp","inputdev.setactivewindow","winui._win32_setactivewindow","winuser/SetActiveWindow"]
old-location: inputdev\setactivewindow.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\setactivewindow.htm
ms.date: 12/05/2018
ms.keywords: SetActiveWindow, SetActiveWindow function [Keyboard and Mouse Input], _win32_SetActiveWindow, _win32_setactivewindow_cpp, inputdev.setactivewindow, winui._win32_setactivewindow, winuser/SetActiveWindow
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
 - SetActiveWindow
 - winuser/SetActiveWindow
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
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - SetActiveWindow
req.apiset: ext-ms-win-ntuser-window-l1-1-4 (introduced in Windows 10, version 10.0.14393)
---

# SetActiveWindow function


## -description

Activates a window. The window must be attached to the calling thread's message queue.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the top-level window to be activated.

## -returns

Type: <b>HWND</b>

If the function succeeds, the return value is the handle to the window that was previously active.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>SetActiveWindow</b> function activates a window, but not if the application is in the background. The window will be brought into the foreground (top of <a href="/windows/desktop/winmsg/window-features">Z-Order</a>) if its application is in the foreground when the system activates the window.

If the window identified by the 
    <i>hWnd</i> parameter was created by the calling thread, the active window status of the calling thread is set to 
    <i>hWnd</i>. Otherwise, the active window status of the calling thread is set to <b>NULL</b>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getactivewindow">GetActiveWindow</a>



<a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setforegroundwindow">SetForegroundWindow</a>



<a href="/windows/desktop/inputdev/wm-activate">WM_ACTIVATE</a>
