---
UID: NF:winuser.GetActiveWindow
title: GetActiveWindow function (winuser.h)
description: Retrieves the window handle to the active window attached to the calling thread's message queue.
helpviewer_keywords: ["GetActiveWindow","GetActiveWindow function [Keyboard and Mouse Input]","_win32_GetActiveWindow","_win32_getactivewindow_cpp","inputdev.getactivewindow","winui._win32_getactivewindow","winuser/GetActiveWindow"]
old-location: inputdev\getactivewindow.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\getactivewindow.htm
ms.date: 12/05/2018
ms.keywords: GetActiveWindow, GetActiveWindow function [Keyboard and Mouse Input], _win32_GetActiveWindow, _win32_getactivewindow_cpp, inputdev.getactivewindow, winui._win32_getactivewindow, winuser/GetActiveWindow
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
 - GetActiveWindow
 - winuser/GetActiveWindow
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
 - Ext-MS-Win-NTUser-Keyboard-l1-1-0.dll
 - Ext-MS-Win-NTUser-Keyboard-l1-1-1.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-keyboard-l1-1-2.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetActiveWindow
req.apiset: ext-ms-win-ntuser-window-l1-1-4 (introduced in Windows 10, version 10.0.14393)
---

# GetActiveWindow function


## -description

Retrieves the window handle to the active window attached to the calling thread's message queue.



## -returns

Type: <b>HWND</b>

The return value is the handle to the active window attached to the calling thread's message queue. Otherwise, the return value is <b>NULL</b>.

## -remarks

To get the handle to the foreground window, you can use <a href="/windows/desktop/api/winuser/nf-winuser-getforegroundwindow">GetForegroundWindow</a>.

To get the window handle to the active window in the message queue for another thread, use <a href="/windows/desktop/api/winuser/nf-winuser-getguithreadinfo">GetGUIThreadInfo</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getforegroundwindow">GetForegroundWindow</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getguithreadinfo">GetGUIThreadInfo</a>



<a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setactivewindow">SetActiveWindow</a>
