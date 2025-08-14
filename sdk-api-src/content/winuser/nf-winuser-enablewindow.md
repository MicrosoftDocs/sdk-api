---
UID: NF:winuser.EnableWindow
title: EnableWindow function (winuser.h)
description: Enables or disables mouse and keyboard input to the specified window or control. When input is disabled, the window does not receive input such as mouse clicks and key presses. When input is enabled, the window receives all input.
helpviewer_keywords: ["EnableWindow","EnableWindow function [Keyboard and Mouse Input]","_win32_EnableWindow","_win32_enablewindow_cpp","inputdev.enablewindow","winui._win32_enablewindow","winuser/EnableWindow"]
old-location: inputdev\enablewindow.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\enablewindow.htm
ms.date: 12/05/2018
ms.keywords: EnableWindow, EnableWindow function [Keyboard and Mouse Input], _win32_EnableWindow, _win32_enablewindow_cpp, inputdev.enablewindow, winui._win32_enablewindow, winuser/EnableWindow
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
 - EnableWindow
 - winuser/EnableWindow
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
 - EnableWindow
req.apiset: ext-ms-win-ntuser-window-l1-1-4 (introduced in Windows 10, version 10.0.14393)
---

# EnableWindow function


## -description

Enables or disables mouse and keyboard input to the specified window or control. When input is disabled, the window does not receive input such as mouse clicks and key presses. When input is enabled, the window receives all input.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window to be enabled or disabled.

### -param bEnable [in]

Type: <b>BOOL</b>

Indicates whether to enable or disable the window. If this parameter is <b>TRUE</b>, the window is enabled. If the parameter is <b>FALSE</b>, the window is disabled.

## -returns

Type: <b>BOOL</b>

If the window was previously disabled, the return value is nonzero.

If the window was not previously disabled, the return value is zero.

## -remarks

If the window is being disabled, the system sends a <a href="/windows/desktop/winmsg/wm-cancelmode">WM_CANCELMODE</a> message. If the enabled state of a window is changing, the system sends a <a href="/windows/desktop/winmsg/wm-enable">WM_ENABLE</a> message after the <b>WM_CANCELMODE</b> message. (These messages are sent before <b>EnableWindow</b> returns.) If a window is already disabled, its child windows are implicitly disabled, although they are not sent a <b>WM_ENABLE</b> message.

A window must be enabled before it can be activated. For example, if an application is displaying a modeless dialog box and has disabled its main window, the application must enable the main window before destroying the dialog box. Otherwise, another window will receive the keyboard focus and be activated. If a child window is disabled, it is ignored when the system tries to determine which window should receive mouse messages.

By default, a window is enabled when it is created. To create a window that is initially disabled, an application can specify the <b>WS_DISABLED</b> style in the <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a> or <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a> function. After a window has been created, an application can use <b>EnableWindow</b> to enable or disable the window.

An application can use this function to enable or disable a control in a dialog box. A disabled control cannot receive the keyboard focus, nor can a user gain access to it.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a>



<a href="/windows/desktop/api/winuser/nf-winuser-iswindowenabled">IsWindowEnabled</a>



<a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/wm-enable">WM_ENABLE</a>
