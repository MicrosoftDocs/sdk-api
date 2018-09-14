---
UID: NF:winuser.BlockInput
title: BlockInput function
author: windows-sdk-content
description: Blocks keyboard and mouse input events from reaching applications.
old-location: inputdev\blockinput.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\blockinput.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: BlockInput, BlockInput function [Keyboard and Mouse Input], _win32_BlockInput, _win32_blockinput_cpp, inputdev.blockinput, winui._win32_blockinput, winuser/BlockInput
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Keyboard-l1-1-0.dll
 - Ext-MS-Win-NTUser-Keyboard-l1-1-1.dll
 - ext-ms-win-ntuser-keyboard-l1-1-2.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-3-0.dll
api_name:
 - BlockInput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

If input is already blocked, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



When input is blocked, real physical input from the mouse or keyboard will not affect the input queue's synchronous key state (reported by <a href="https://msdn.microsoft.com/41c7bcc7-0a14-420c-b338-7ca13c95b7b8">GetKeyState</a> and <a href="https://msdn.microsoft.com/d6b31d2c-43b3-4502-a7ed-af564895f27e">GetKeyboardState</a>), nor will it affect the asynchronous key state (reported by <a href="https://msdn.microsoft.com/edc449e4-f37d-4f2c-8add-45b905bd3326">GetAsyncKeyState</a>). However, the thread that is blocking input can affect both of these key states by calling <a href="https://msdn.microsoft.com/7f87edd0-b846-4a85-93c8-9a2eeda7b6ac">SendInput</a>. No other thread can do this.

The system will unblock input in the following cases:

<ul>
<li>The thread that blocked input unexpectedly exits without calling <b>BlockInput</b> with 
      <i>fBlock</i> set to <b>FALSE</b>. In this case, the system cleans up properly and re-enables input.</li>
<li>The user presses CTRL+ALT+DEL or the system invokes the 
      <b>Hard System Error</b> modal message box (for example, when a program faults or a device fails).</li>
</ul>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/edc449e4-f37d-4f2c-8add-45b905bd3326">GetAsyncKeyState</a>



<a href="https://msdn.microsoft.com/41c7bcc7-0a14-420c-b338-7ca13c95b7b8">GetKeyState</a>



<a href="https://msdn.microsoft.com/d6b31d2c-43b3-4502-a7ed-af564895f27e">GetKeyboardState</a>



<a href="https://msdn.microsoft.com/a3f6ac32-cde9-440d-bbde-0d76b4b5d4a4">Keyboard Input</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/7f87edd0-b846-4a85-93c8-9a2eeda7b6ac">SendInput</a>
 

 

