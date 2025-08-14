---
UID: NF:winuser.SetKeyboardState
title: SetKeyboardState function (winuser.h)
description: Copies an array of keyboard key states into the calling thread's keyboard input-state table. This is the same table accessed by the GetKeyboardState and GetKeyState functions. Changes made to this table do not affect keyboard input to any other thread.
helpviewer_keywords: ["SetKeyboardState","SetKeyboardState function [Keyboard and Mouse Input]","_win32_SetKeyboardState","_win32_setkeyboardstate_cpp","inputdev.setkeyboardstate","winui._win32_setkeyboardstate","winuser/SetKeyboardState"]
old-location: inputdev\setkeyboardstate.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\setkeyboardstate.htm
ms.date: 12/05/2018
ms.keywords: SetKeyboardState, SetKeyboardState function [Keyboard and Mouse Input], _win32_SetKeyboardState, _win32_setkeyboardstate_cpp, inputdev.setkeyboardstate, winui._win32_setkeyboardstate, winuser/SetKeyboardState
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
 - SetKeyboardState
 - winuser/SetKeyboardState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-keyboard-l1-3-2.dll
 - ext-ms-win-ntuser-keyboard-l1-3-1.dll
 - User32.dll
 - ext-ms-win-ntuser-keyboard-l1-1-2.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-3-0.dll
api_name:
 - SetKeyboardState
---

# SetKeyboardState function


## -description

Copies an array of keyboard key states into the calling thread's keyboard input-state table. This is the same table accessed by the <a href="/windows/desktop/api/winuser/nf-winuser-getkeyboardstate">GetKeyboardState</a> and <a href="/windows/desktop/api/winuser/nf-winuser-getkeystate">GetKeyState</a> functions. Changes made to this table do not affect keyboard input to any other thread.

## -parameters

### -param lpKeyState [in]

Type: <b>LPBYTE</b>

A pointer to a 256-byte array that contains keyboard key states.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Because the <b>SetKeyboardState</b> function alters the input state of the calling thread and not the global input state of the system, an application cannot use <b>SetKeyboardState</b> to set the NUM LOCK, CAPS LOCK, or SCROLL LOCK (or the Japanese KANA) indicator lights on the keyboard. These can be set or cleared using <a href="/windows/desktop/api/winuser/nf-winuser-sendinput">SendInput</a> to simulate keystrokes.

## -see-also

- <a href="/windows/desktop/api/winuser/nf-winuser-getasynckeystate">GetAsyncKeyState</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-getkeystate">GetKeyState</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-getkeyboardstate">GetKeyboardState</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-mapvirtualkeya">MapVirtualKey</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-setkeyboardstate">SetKeyboardState</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-sendinput">SendInput</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-keybd_event">keybd_event</a>
- <a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>
