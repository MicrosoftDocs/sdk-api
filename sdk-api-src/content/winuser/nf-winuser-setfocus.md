---
UID: NF:winuser.SetFocus
title: SetFocus function
author: windows-sdk-content
description: Sets the keyboard focus to the specified window. The window must be attached to the calling thread's message queue.
old-location: inputdev\setfocus.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\setfocus.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetFocus, SetFocus function [Keyboard and Mouse Input], _win32_SetFocus, _win32_setfocus_cpp, inputdev.setfocus, winui._win32_setfocus, winuser/SetFocus
ms.prod: windows-hardware
ms.technology: windows-devices
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetFocus function


## -description


Sets the keyboard focus to the specified window. The window must be attached to the calling thread's message queue.


## -parameters




### -param hWnd [in, optional]

Type: <b>HWND</b>

A handle to the window that will receive the keyboard input. If this parameter is <b>NULL</b>, keystrokes are ignored.


## -returns



Type: <b>HWND</b>

If the function succeeds, the return value is the handle to the window that previously had the keyboard focus. If the 
      <i>hWnd</i> parameter is invalid or the window is not attached to the calling thread's message queue, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>SetFocus</b> function sends a <a href="https://msdn.microsoft.com/en-us/library/ms646282(v=VS.85).aspx">WM_KILLFOCUS</a> message to the window that loses the keyboard focus and a <a href="https://msdn.microsoft.com/en-us/library/ms646283(v=VS.85).aspx">WM_SETFOCUS</a> message to the window that receives the keyboard focus. It also activates either the window that receives the focus or the parent of the window that receives the focus.

If a window is active but does not have the focus, any key pressed will produce the <a href="https://msdn.microsoft.com/en-us/library/ms646357(v=VS.85).aspx">WM_SYSCHAR</a>, <a href="https://msdn.microsoft.com/en-us/library/ms646286(v=VS.85).aspx">WM_SYSKEYDOWN</a>, or <a href="https://msdn.microsoft.com/en-us/library/ms646287(v=VS.85).aspx">WM_SYSKEYUP</a> message. If the <b>VK_MENU</b> key is also pressed, the

    <i>lParam</i> parameter of the message will have bit 30 set. Otherwise, the messages produced do not have this bit set.

By using the 
    <a href="https://msdn.microsoft.com/0c343fab-56ae-4c70-a79e-0c5f827158a3">AttachThreadInput</a> function, a thread can attach its input processing to another thread. This allows a thread to call <b>SetFocus</b> to set the keyboard focus to a window attached to another thread's message queue.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms644996(v=VS.85).aspx">Initializing a Dialog Box</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0c343fab-56ae-4c70-a79e-0c5f827158a3">AttachThreadInput</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646294(v=VS.85).aspx">GetFocus</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645530(v=VS.85).aspx">Keyboard Input</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646282(v=VS.85).aspx">WM_KILLFOCUS</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646283(v=VS.85).aspx">WM_SETFOCUS</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646357(v=VS.85).aspx">WM_SYSCHAR</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646286(v=VS.85).aspx">WM_SYSKEYDOWN</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646287(v=VS.85).aspx">WM_SYSKEYUP</a>
 

 

