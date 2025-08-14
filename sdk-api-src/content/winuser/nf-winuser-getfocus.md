---
UID: NF:winuser.GetFocus
title: GetFocus function (winuser.h)
description: Retrieves the handle to the window that has the keyboard focus, if the window is attached to the calling thread's message queue.
helpviewer_keywords: ["GetFocus","GetFocus function [Keyboard and Mouse Input]","_win32_GetFocus","_win32_getfocus_cpp","inputdev.getfocus","winui._win32_getfocus","winuser/GetFocus"]
old-location: inputdev\getfocus.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\getfocus.htm
ms.date: 12/05/2018
ms.keywords: GetFocus, GetFocus function [Keyboard and Mouse Input], _win32_GetFocus, _win32_getfocus_cpp, inputdev.getfocus, winui._win32_getfocus, winuser/GetFocus
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
 - GetFocus
 - winuser/GetFocus
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
 - GetFocus
req.apiset: ext-ms-win-ntuser-window-l1-1-4 (introduced in Windows 10, version 10.0.14393)
---

# GetFocus function


## -description

Retrieves the handle to the window that has the keyboard focus, if the window is attached to the calling thread's message queue.



## -returns

Type: <b>HWND</b>

The return value is the handle to the window with the keyboard focus. If the calling thread's message queue does not have an associated window with the keyboard focus, the return value is <b>NULL</b>.

## -remarks

<b>GetFocus</b> returns the window with the keyboard focus for the current thread's message queue. If <b>GetFocus</b> returns <b>NULL</b>, another thread's queue may be attached to a window that has the keyboard focus.

Use the <a href="/windows/desktop/api/winuser/nf-winuser-getforegroundwindow">GetForegroundWindow</a> function to retrieve the handle to the window with which the user is currently working. You can associate your thread's message queue with the windows owned by another thread by using the 
    <a href="/windows/desktop/api/winuser/nf-winuser-attachthreadinput">AttachThreadInput</a> function.

To get the window with the keyboard focus on the foreground queue or the queue of another thread, use the <a href="/windows/desktop/api/winuser/nf-winuser-getguithreadinfo">GetGUIThreadInfo</a> function.


#### Examples

For an example, see "Creating a Combo Box Toolbar" in <a href="/windows/desktop/Controls/using-combo-boxes">Using Combo Boxes</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-attachthreadinput">AttachThreadInput</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getforegroundwindow">GetForegroundWindow</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getguithreadinfo">GetGUIThreadInfo</a>



<a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setfocus">SetFocus</a>



<a href="/windows/desktop/inputdev/wm-killfocus">WM_KILLFOCUS</a>



<a href="/windows/desktop/inputdev/wm-setfocus">WM_SETFOCUS</a>
