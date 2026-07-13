---
UID: NF:winuser.SetCapture
title: SetCapture function (winuser.h)
description: Sets the mouse capture to the specified window belonging to the current thread.
helpviewer_keywords: ["SetCapture","SetCapture function [Keyboard and Mouse Input]","_win32_SetCapture","_win32_setcapture_cpp","inputdev.setcapture","winui._win32_setcapture","winuser/SetCapture"]
old-location: inputdev\setcapture.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputfunctions\setcapture.htm
ms.date: 12/05/2018
ms.keywords: SetCapture, SetCapture function [Keyboard and Mouse Input], _win32_SetCapture, _win32_setcapture_cpp, inputdev.setcapture, winui._win32_setcapture, winuser/SetCapture
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
 - SetCapture
 - winuser/SetCapture
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-mouse-l1-1-0.dll
 - ext-ms-win-ntuser-mouse-l1-1-1.dll
 - User32.dll
 - Ext-MS-Win-NTUser-mouse-l1-1-0.dll
 - api-ms-win-ntuser-ie-mouse-l1-1-0.dll
 - ie_stubs.dll
api_name:
 - SetCapture
req.apiset: ext-ms-win-ntuser-mouse-l1-1-0 (introduced in Windows 8)
---

# SetCapture function


## -description

Sets the mouse capture to the specified window belonging to the current thread. <b>SetCapture</b> captures mouse input either when the mouse is over the capturing window, or when the mouse button was pressed while the mouse was over the capturing window and the button is still down. Only one window at a time can capture the mouse.

If the mouse cursor is over a window created by another thread, the system will direct mouse input to the specified window only if a mouse button is down.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window in the current thread that is to capture the mouse.

## -returns

Type: <b>HWND</b>

The return value is a handle to the window that had previously captured the mouse. If there is no such window, the return value is <b>NULL</b>.

## -remarks

Only the foreground window can capture the mouse. When a background window attempts to do so, the window receives messages only for mouse events that occur when the cursor hot spot is within the visible portion of the window. Also, even if the foreground window has captured the mouse, the user can still click another window, bringing it to the foreground. 

When the window no longer requires all mouse input, the thread that created the window should call the <a href="/windows/desktop/api/winuser/nf-winuser-releasecapture">ReleaseCapture</a> function to release the mouse. 

This function cannot be used to capture mouse input meant for another process. 

When the mouse is captured, menu hotkeys and other keyboard accelerators do not work. 


#### Examples

For an example, see <a href="/windows/desktop/inputdev/using-mouse-input">Drawing Lines with the Mouse</a>.

<div class="code"></div>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getcapture">GetCapture</a>



<a href="/windows/desktop/inputdev/mouse-input">Mouse Input</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-releasecapture">ReleaseCapture</a>



<a href="/windows/desktop/inputdev/wm-capturechanged">WM_CAPTURECHANGED</a>
