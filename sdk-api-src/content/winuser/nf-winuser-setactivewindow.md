---
UID: NF:winuser.SetActiveWindow
title: SetActiveWindow function
author: windows-sdk-content
description: Activates a window. The window must be attached to the calling thread's message queue.
old-location: inputdev\setactivewindow.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\setactivewindow.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: SetActiveWindow, SetActiveWindow function [Keyboard and Mouse Input], _win32_SetActiveWindow, _win32_setactivewindow_cpp, inputdev.setactivewindow, winui._win32_setactivewindow, winuser/SetActiveWindow
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
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - SetActiveWindow
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetActiveWindow function


## -description


Activates a window. The window must be attached to the calling thread's message queue.


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the top-level window to be activated.


## -returns



Type: <b>HWND</b>

If the function succeeds, the return value is the handle to the window that was previously active.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>SetActiveWindow</b> function activates a window, but not if the application is in the background. The window will be brought into the foreground (top of <a href="https://msdn.microsoft.com/8318c22f-85a2-490e-8233-ee1e234890d9">Z-Order</a>) if its application is in the foreground when the system activates the window.

If the window identified by the 
    <i>hWnd</i> parameter was created by the calling thread, the active window status of the calling thread is set to 
    <i>hWnd</i>. Otherwise, the active window status of the calling thread is set to <b>NULL</b>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/48f5ed0f-d141-4fef-8f34-7107156e2f48">GetActiveWindow</a>



<a href="https://msdn.microsoft.com/a3f6ac32-cde9-440d-bbde-0d76b4b5d4a4">Keyboard Input</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/c728ff42-1a5e-45c9-b2ab-5e28ad430a2d">SetForegroundWindow</a>



<a href="https://msdn.microsoft.com/a62bb9f7-f286-4d0d-a1ca-370950c188b2">WM_ACTIVATE</a>
 

 

