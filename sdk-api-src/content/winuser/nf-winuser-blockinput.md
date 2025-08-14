---
UID: NF:winuser.BlockInput
title: BlockInput function (winuser.h)
description: Blocks keyboard and mouse input events from reaching applications.
helpviewer_keywords: ["BlockInput","BlockInput function [Keyboard and Mouse Input]","_win32_BlockInput","_win32_blockinput_cpp","inputdev.blockinput","winui._win32_blockinput","winuser/BlockInput"]
old-location: inputdev\blockinput.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\blockinput.htm
ms.date: 12/05/2018
ms.keywords: BlockInput, BlockInput function [Keyboard and Mouse Input], _win32_BlockInput, _win32_blockinput_cpp, inputdev.blockinput, winui._win32_blockinput, winuser/BlockInput
req.header: winuser.h
req.include-header: 
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
 - BlockInput
 - winuser/BlockInput
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
 - Ext-MS-Win-NTUser-Keyboard-l1-1-0.dll
 - Ext-MS-Win-NTUser-Keyboard-l1-1-1.dll
 - ext-ms-win-ntuser-keyboard-l1-1-2.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-3-0.dll
api_name:
 - BlockInput
---

# BlockInput function


## -description

Blocks keyboard and mouse input events from reaching applications.

## -parameters

### -param fBlockIt [in]

Type: <b>BOOL</b>

The function's purpose. If this parameter is <b>TRUE</b>, keyboard and mouse input events are blocked. If this parameter is <b>FALSE</b>, keyboard and mouse events are unblocked. Note that only the thread that blocked input can successfully unblock input.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If input is already blocked, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

When input is blocked, real physical input from the mouse or keyboard will not affect the input queue's synchronous key state (reported by <a href="/windows/desktop/api/winuser/nf-winuser-getkeystate">GetKeyState</a> and <a href="/windows/desktop/api/winuser/nf-winuser-getkeyboardstate">GetKeyboardState</a>), nor will it affect the asynchronous key state (reported by <a href="/windows/desktop/api/winuser/nf-winuser-getasynckeystate">GetAsyncKeyState</a>). However, the thread that is blocking input can affect both of these key states by calling <a href="/windows/desktop/api/winuser/nf-winuser-sendinput">SendInput</a>. No other thread can do this.

The system will unblock input in the following cases:

<ul>
<li>The thread that blocked input unexpectedly exits without calling <b>BlockInput</b> with 
      <i>fBlock</i> set to <b>FALSE</b>. In this case, the system cleans up properly and re-enables input.</li>
<li>The user presses CTRL+ALT+DEL or the system invokes the 
      <b>Hard System Error</b> modal message box (for example, when a program faults or a device fails).</li>
</ul>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getasynckeystate">GetAsyncKeyState</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getkeystate">GetKeyState</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getkeyboardstate">GetKeyboardState</a>



<a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-sendinput">SendInput</a>