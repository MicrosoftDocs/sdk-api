---
UID: NF:winuser.SetCapture
title: SetCapture function
author: windows-sdk-content
description: Sets the mouse capture to the specified window belonging to the current thread.
old-location: inputdev\setcapture.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputfunctions\setcapture.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SetCapture, SetCapture function [Keyboard and Mouse Input], _win32_SetCapture, _win32_setcapture_cpp, inputdev.setcapture, winui._win32_setcapture, winuser/SetCapture
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
 - Ext-MS-Win-NTUser-mouse-l1-1-0.dll
 - api-ms-win-ntuser-ie-mouse-l1-1-0.dll
 - ie_stubs.dll
api_name:
 - SetCapture
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetCapture function


## -description


Sets the mouse capture to the specified window belonging to the current thread.<b>SetCapture</b> captures mouse input either when the mouse is over the capturing window, or when the mouse button was pressed while the mouse was over the capturing window and the button is still down. Only one window at a time can capture the mouse.

If the mouse cursor is over a window created by another thread, the system will direct mouse input to the specified window only if a mouse button is down.


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window in the current thread that is to capture the mouse. 


## -returns



Type: <b>HWND</b>

The return value is a handle to the window that had previously captured the mouse. If there is no such window, the return value is <b>NULL</b>. 




## -remarks



Only the foreground window can capture the mouse. When a background window attempts to do so, the window receives messages only for mouse events that occur when the cursor hot spot is within the visible portion of the window. Also, even if the foreground window has captured the mouse, the user can still click another window, bringing it to the foreground. 

When the window no longer requires all mouse input, the thread that created the window should call the <a href="https://msdn.microsoft.com/43e1f766-35b1-451d-9921-c1d4eebc4435">ReleaseCapture</a> function to release the mouse. 

This function cannot be used to capture mouse input meant for another process. 

When the mouse is captured, menu hotkeys and other keyboard accelerators do not work. 


#### Examples

For an example, see <a href="using_mouse_input.htm">Drawing Lines with the Mouse</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/cb35a155-f66c-4dc2-9358-d1065ec9c894">GetCapture</a>



<a href="https://msdn.microsoft.com/35f5e1ad-74d5-41bb-9016-b1c5de449550">Mouse Input</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/43e1f766-35b1-451d-9921-c1d4eebc4435">ReleaseCapture</a>



<a href="https://msdn.microsoft.com/79c8f65e-31fa-4bdb-9e88-0160a52b5b7d">WM_CAPTURECHANGED</a>
 

 

