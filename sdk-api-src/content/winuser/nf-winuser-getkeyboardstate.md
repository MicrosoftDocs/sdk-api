---
UID: NF:winuser.GetKeyboardState
title: GetKeyboardState function (winuser.h)
description: Copies the status of the 256 virtual keys to the specified buffer.
helpviewer_keywords: ["GetKeyboardState","GetKeyboardState function [Keyboard and Mouse Input]","_win32_GetKeyboardState","_win32_getkeyboardstate_cpp","inputdev.getkeyboardstate","winui._win32_getkeyboardstate","winuser/GetKeyboardState"]
old-location: inputdev\getkeyboardstate.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\getkeyboardstate.htm
ms.date: 12/05/2018
ms.keywords: GetKeyboardState, GetKeyboardState function [Keyboard and Mouse Input], _win32_GetKeyboardState, _win32_getkeyboardstate_cpp, inputdev.getkeyboardstate, winui._win32_getkeyboardstate, winuser/GetKeyboardState
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
 - GetKeyboardState
 - winuser/GetKeyboardState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-rawinput-l1-1-1.dll
 - ext-ms-win-ntuser-keyboard-l1-3-2.dll
 - ext-ms-win-ntuser-keyboard-l1-3-1.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Keyboard-l1-1-0.dll
 - Ext-MS-Win-NTUser-Keyboard-l1-1-1.dll
 - api-ms-win-ntuser-ie-keyboard-l1-1-0.dll
 - ie_stubs.dll
 - ext-ms-win-ntuser-keyboard-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Rawinput-L1-1-0.dll
 - MinUser.dll
api_name:
 - GetKeyboardState
req.apiset: ext-ms-win-ntuser-rawinput-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# GetKeyboardState function


## -description

Copies the status of the 256 virtual keys to the specified buffer.

## -parameters

### -param lpKeyState [out]

Type: <b>PBYTE</b>

The 256-byte array that receives the status data for each virtual key.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

An application can call this function to retrieve the current status of all the virtual keys. The status changes as a thread removes keyboard messages from its message queue. The status does not change as keyboard messages are posted to the thread's message queue, nor does it change as keyboard messages are posted to or retrieved from message queues of other threads. (Exception: Threads that are connected through <a href="/windows/desktop/api/winuser/nf-winuser-attachthreadinput">AttachThreadInput</a> share the same keyboard state.)

When the function returns, each member of the array pointed to by the 
				<i>lpKeyState</i> parameter contains status data for a virtual key. If the high-order bit is 1, the key is down; otherwise, it is up. If the key is a toggle key, for example CAPS LOCK, then the low-order bit is 1 when the key is toggled and is 0 if the key is untoggled.  The low-order bit is meaningless for non-toggle keys. A toggle key is said to be toggled when it is turned on.
A toggle key's indicator light (if any) on the keyboard will be on when the key is toggled, and off when the key is untoggled. 

To retrieve status information for an individual key, use the <a href="/windows/desktop/api/winuser/nf-winuser-getkeystate">GetKeyState</a> function. To retrieve the current state for an individual key regardless of whether the corresponding keyboard message has been retrieved from the message queue, use the <a href="/windows/desktop/api/winuser/nf-winuser-getasynckeystate">GetAsyncKeyState</a> function.

An application can use the virtual-key code constants <b>VK_SHIFT</b>, <b>VK_CONTROL</b> and <b>VK_MENU</b> as indices into the array pointed to by 
				<i>lpKeyState</i>. This gives the status of the SHIFT, CTRL, or ALT keys without distinguishing between left and right. An application can also use the following virtual-key code constants as indices to distinguish between the left and right instances of those keys: 

<table class="clsStd">
<tr>
<td><b>VK_LSHIFT</b></td>
</tr>
<tr>
<td><b>VK_RSHIFT</b></td>
</tr>
<tr>
<td><b>VK_LCONTROL</b></td>
</tr>
<tr>
<td><b>VK_RCONTROL</b></td>
</tr>
<tr>
<td><b>VK_LMENU</b></td>
</tr>
<tr>
<td><b>VK_RMENU</b></td>
</tr>
</table>
 

These left- and right-distinguishing constants are available to an application only through the <b>GetKeyboardState</b>, <a href="/windows/desktop/api/winuser/nf-winuser-setkeyboardstate">SetKeyboardState</a>, <a href="/windows/desktop/api/winuser/nf-winuser-getasynckeystate">GetAsyncKeyState</a>, <a href="/windows/desktop/api/winuser/nf-winuser-getkeystate">GetKeyState</a>, and <a href="/windows/desktop/api/winuser/nf-winuser-mapvirtualkeya">MapVirtualKey</a> functions.

## -see-also

- <a href="/windows/desktop/api/winuser/nf-winuser-getasynckeystate">GetAsyncKeyState</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-getkeystate">GetKeyState</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-getkeyboardstate">GetKeyboardState</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-mapvirtualkeya">MapVirtualKey</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-setkeyboardstate">SetKeyboardState</a>
- <a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>
