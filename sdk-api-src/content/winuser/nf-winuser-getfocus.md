---
UID: NF:winuser.GetFocus
title: GetFocus function
author: windows-sdk-content
description: Retrieves the handle to the window that has the keyboard focus, if the window is attached to the calling thread's message queue.
old-location: inputdev\getfocus.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\getfocus.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetFocus, GetFocus function [Keyboard and Mouse Input], _win32_GetFocus, _win32_getfocus_cpp, inputdev.getfocus, winui._win32_getfocus, winuser/GetFocus
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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

Use the <a href="https://msdn.microsoft.com/ee30a5fc-a229-4b84-b1f7-2d071d641a22">GetForegroundWindow</a> function to retrieve the handle to the window with which the user is currently working. You can associate your thread's message queue with the windows owned by another thread by using the 
    <a href="https://msdn.microsoft.com/0c343fab-56ae-4c70-a79e-0c5f827158a3">AttachThreadInput</a> function.

To get the window with the keyboard focus on the foreground queue or the queue of another thread, use the <a href="https://msdn.microsoft.com/863e0735-a2d4-4962-99d8-bb6037770c50">GetGUIThreadInfo</a> function.


#### Examples

For an example, see "Creating a Combo Box Toolbar" in <a href="_win32_Using_Combo_Boxes">Using Combo Boxes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0c343fab-56ae-4c70-a79e-0c5f827158a3">AttachThreadInput</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/ee30a5fc-a229-4b84-b1f7-2d071d641a22">GetForegroundWindow</a>



<a href="https://msdn.microsoft.com/863e0735-a2d4-4962-99d8-bb6037770c50">GetGUIThreadInfo</a>



<a href="https://msdn.microsoft.com/a3f6ac32-cde9-440d-bbde-0d76b4b5d4a4">Keyboard Input</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/88fc2959-007a-441d-8a02-19d775f28de9">SetFocus</a>



<a href="https://msdn.microsoft.com/6d32a09b-a856-4f94-9544-3345b3a700f4">WM_KILLFOCUS</a>



<a href="https://msdn.microsoft.com/77180e4c-95a6-41a4-93d9-033381ae7543">WM_SETFOCUS</a>
 

 

