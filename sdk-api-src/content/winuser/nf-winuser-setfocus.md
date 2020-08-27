---
UID: NF:winuser.SetFocus
title: SetFocus function (winuser.h)
description: Sets the keyboard focus to the specified window. The window must be attached to the calling thread's message queue.
helpviewer_keywords: ["SetFocus","SetFocus function [Keyboard and Mouse Input]","_win32_SetFocus","_win32_setfocus_cpp","inputdev.setfocus","winui._win32_setfocus","winuser/SetFocus"]
old-location: inputdev\setfocus.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\setfocus.htm
ms.date: 12/05/2018
ms.keywords: SetFocus, SetFocus function [Keyboard and Mouse Input], _win32_SetFocus, _win32_setfocus_cpp, inputdev.setfocus, winui._win32_setfocus, winuser/SetFocus
f1_keywords:
- winuser/SetFocus
dev_langs:
- c++
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
- Ext-MS-Win-NTUser-Keyboard-l1-1-0.dll
- Ext-MS-Win-NTUser-Keyboard-l1-1-1.dll
- Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
- ext-ms-win-ntuser-keyboard-l1-1-2.dll
- Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
- Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
- Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
- SetFocus
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetFocus function

## -description

Sets the keyboard focus to the specified window. The window must be attached to the calling thread's message queue.

## -parameters

### -param hWnd [in, optional]

Type: **HWND**

A handle to the window that will receive the keyboard input. If this parameter is NULL, keystrokes are ignored.

## -returns

Type: **HWND**

If the function succeeds, the return value is the handle to the window that previously had the keyboard focus. If the *hWnd* parameter is invalid or the window is not attached to the calling thread's message queue, the return value is NULL. To get extended error information, call [GetLastError function](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

## -remarks

This function sends a [WM_KILLFOCUS](https://docs.microsoft.com/windows/desktop/inputdev/wm-killfocus) message to the window that loses the keyboard focus and a [WM_SETFOCUS](https://docs.microsoft.com/windows/desktop/inputdev/wm-setfocus) message to the window that receives the keyboard focus. It also activates either the window that receives the focus or the parent of the window that receives the focus.

If a window is active but does not have the focus, any key pressed produces the [WM_SYSCHAR](https://docs.microsoft.com/windows/desktop/menurc/wm-syschar), [WM_SYSKEYDOWN](https://docs.microsoft.com/windows/desktop/inputdev/wm-syskeydown), or [WM_SYSKEYUP](https://docs.microsoft.com/windows/desktop/inputdev/wm-syskeyup) message. If the VK_MENU key is also pressed, bit 30 of the *lParam* parameter of the message is set. Otherwise, the messages produced do not have this bit set.

By using the [AttachThreadInput function](nf-winuser-attachthreadinput.md), a thread can attach its input processing to another thread. This allows a thread to call SetFocus to set the keyboard focus to a window attached to another thread's message queue.

### Examples

For an example, see [Initializing a Dialog Box](https://docs.microsoft.com/windows/desktop/dlgbox/using-dialog-boxes).

## -see-also

[AttachThreadInput function](nf-winuser-attachthreadinput.md), [GetFocus function](nf-winuser-getfocus.md), [WM_KILLFOCUS](https://docs.microsoft.com/windows/desktop/inputdev/wm-killfocus), [WM_SETFOCUS](https://docs.microsoft.com/windows/desktop/inputdev/wm-setfocus), [WM_SYSCHAR](https://docs.microsoft.com/windows/desktop/menurc/wm-syschar), [WM_SYSKEYDOWN](https://docs.microsoft.com/windows/desktop/inputdev/wm-syskeydown), [WM_SYSKEYUP](https://docs.microsoft.com/windows/desktop/inputdev/wm-syskeyup), [Keyboard Input](https://docs.microsoft.com/windows/desktop/inputdev/keyboard-input)
