---
UID: NF:winuser.SetKeyboardState
title: SetKeyboardState function
author: windows-sdk-content
description: Copies an array of keyboard key states into the calling thread's keyboard input-state table. This is the same table accessed by the GetKeyboardState and GetKeyState functions. Changes made to this table do not affect keyboard input to any other thread.
old-location: inputdev\setkeyboardstate.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\setkeyboardstate.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetKeyboardState, SetKeyboardState function [Keyboard and Mouse Input], _win32_SetKeyboardState, _win32_setkeyboardstate_cpp, inputdev.setkeyboardstate, winui._win32_setkeyboardstate, winuser/SetKeyboardState
ms.topic: function
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
 - ext-ms-win-ntuser-keyboard-l1-1-2.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-3-0.dll
api_name:
 - SetKeyboardState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetKeyboardState function


## -description


Copies an array of keyboard key states into the calling thread's keyboard input-state table. This is the same table accessed by the <a href="https://msdn.microsoft.com/en-us/library/ms646299(v=VS.85).aspx">GetKeyboardState</a> and <a href="https://msdn.microsoft.com/en-us/library/ms646301(v=VS.85).aspx">GetKeyState</a> functions. Changes made to this table do not affect keyboard input to any other thread.


## -parameters




### -param lpKeyState [in]

Type: <b>LPBYTE</b>

A pointer to a 256-byte array that contains keyboard key states.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Because the <b>SetKeyboardState</b> function alters the input state of the calling thread and not the global input state of the system, an application cannot use <b>SetKeyboardState</b> to set the NUM LOCK, CAPS LOCK, or SCROLL LOCK (or the Japanese KANA) indicator lights on the keyboard. These can be set or cleared using <a href="https://msdn.microsoft.com/en-us/library/ms646310(v=VS.85).aspx">SendInput</a> to simulate keystrokes.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646293(v=VS.85).aspx">GetAsyncKeyState</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646301(v=VS.85).aspx">GetKeyState</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646299(v=VS.85).aspx">GetKeyboardState</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645530(v=VS.85).aspx">Keyboard Input</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646306(v=VS.85).aspx">MapVirtualKey</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646310(v=VS.85).aspx">SendInput</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646304(v=VS.85).aspx">keybd_event</a>
 

 

