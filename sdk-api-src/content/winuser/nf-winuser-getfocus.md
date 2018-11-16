---
UID: NF:winuser.GetFocus
title: GetFocus function
author: windows-sdk-content
description: Retrieves the handle to the window that has the keyboard focus, if the window is attached to the calling thread's message queue.
old-location: inputdev\getfocus.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\getfocus.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetFocus, GetFocus function [Keyboard and Mouse Input], _win32_GetFocus, _win32_getfocus_cpp, inputdev.getfocus, winui._win32_getfocus, winuser/GetFocus
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
 - GetFocus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetFocus
: 
---

# GetFocus function


## -description


Retrieves the handle to the window that has the keyboard focus, if the window is attached to the calling thread's message queue.


## -parameters






## -returns



Type: <b>HWND</b>

The return value is the handle to the window with the keyboard focus. If the calling thread's message queue does not have an associated window with the keyboard focus, the return value is <b>NULL</b>.




## -remarks



<b>GetFocus</b> returns the window with the keyboard focus for the current thread's message queue. If <b>GetFocus</b> returns <b>NULL</b>, another thread's queue may be attached to a window that has the keyboard focus.

Use the <a href="https://msdn.microsoft.com/en-us/library/ms633505(v=VS.85).aspx">GetForegroundWindow</a> function to retrieve the handle to the window with which the user is currently working. You can associate your thread's message queue with the windows owned by another thread by using the 
    <a href="https://msdn.microsoft.com/0c343fab-56ae-4c70-a79e-0c5f827158a3">AttachThreadInput</a> function.

To get the window with the keyboard focus on the foreground queue or the queue of another thread, use the <a href="https://msdn.microsoft.com/en-us/library/ms633506(v=VS.85).aspx">GetGUIThreadInfo</a> function.


#### Examples

For an example, see "Creating a Combo Box Toolbar" in <a href="https://msdn.microsoft.com/en-us/library/Bb775794(v=VS.85).aspx">Using Combo Boxes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0c343fab-56ae-4c70-a79e-0c5f827158a3">AttachThreadInput</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633505(v=VS.85).aspx">GetForegroundWindow</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633506(v=VS.85).aspx">GetGUIThreadInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645530(v=VS.85).aspx">Keyboard Input</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646312(v=VS.85).aspx">SetFocus</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646282(v=VS.85).aspx">WM_KILLFOCUS</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646283(v=VS.85).aspx">WM_SETFOCUS</a>
 

 

