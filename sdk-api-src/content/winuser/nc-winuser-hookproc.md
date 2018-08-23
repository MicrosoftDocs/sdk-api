---
UID: NC:winuser.HOOKPROC
title: HOOKPROC
author: windows-sdk-content
description: An application-defined or library-defined callback function used with the SetWindowsHookEx function. The system calls this function before calling the window procedure to process a message sent to the thread.
old-location: winmsg\callwndproc.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookfunctions\callwndproc.htm
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: CallWndProc, CallWndProc callback, CallWndProc callback function [Windows and Messages], HOOKPROC, _win32_CallWndProc, _win32_callwndproc_cpp, winmsg.callwndproc, winui._win32_callwndproc, winuser/CallWndProc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
req.typenames: WINUSB_PIPE_INFORMATION_EX, *PWINUSB_PIPE_INFORMATION_EX
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winuser.h
api_name:
 - CallWndProc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# HOOKPROC callback function


## -description


An application-defined or library-defined callback function used with the <a href="https://msdn.microsoft.com/en-us/library/ms644990(v=VS.85).aspx">SetWindowsHookEx</a> function. 

			The system calls this function before calling the window procedure to process a message sent to the thread.

The <b>HOOKPROC</b> type defines a pointer to this callback function. <i>CallWndProc</i> is a placeholder for the application-defined or library-defined function name.


## -parameters




### -param code


### -param wParam [in]

Type: <b>WPARAM</b>

Specifies whether the message was sent by the current thread. If the message was sent by the current thread, it is nonzero; otherwise, it is zero. 


### -param lParam [in]

Type: <b>LPARAM</b>

A pointer to a <a href="https://msdn.microsoft.com/5c115d25-91a5-41e8-bce0-cf03b51da272">CWPSTRUCT</a> structure that contains details about the message. 


#### - nCode [in]

Type: <b>int</b>

Specifies whether the hook procedure must process the message. If <i>nCode</i> is <b>HC_ACTION</b>, the hook procedure must process the message. If 	<i>nCode</i> is less than zero, the hook procedure must pass the message to the <a href="https://msdn.microsoft.com/en-us/library/ms644974(v=VS.85).aspx">CallNextHookEx</a> function without further processing and must return the value returned by <b>CallNextHookEx</b>. 


## -returns



Type: <strong>Type: <b>LRESULT</b>
</strong>

If <i>nCode</i> is less than zero, the hook procedure must return the value returned by <a href="https://msdn.microsoft.com/en-us/library/ms644974(v=VS.85).aspx">CallNextHookEx</a>. 

If <i>nCode</i> is greater than or equal to zero, it is highly recommended that you call <a href="https://msdn.microsoft.com/en-us/library/ms644974(v=VS.85).aspx">CallNextHookEx</a> and return the value it returns; otherwise, other applications that have installed <a href="about_hooks.htm">WH_CALLWNDPROC</a> hooks will not receive hook notifications and may behave incorrectly as a result. If the hook procedure does not call <b>CallNextHookEx</b>, the return value should be zero. 




## -remarks



The <i>CallWndProc</i> hook procedure can examine the message, but it cannot modify it. After the hook procedure returns control to the system, the message is passed to the window procedure. 

An application installs the hook procedure by specifying the <a href="about_hooks.htm">WH_CALLWNDPROC</a> hook type and a pointer to the hook procedure in a call to the <a href="https://msdn.microsoft.com/en-us/library/ms644990(v=VS.85).aspx">SetWindowsHookEx</a> function. 




## -see-also




<a href="https://msdn.microsoft.com/5c115d25-91a5-41e8-bce0-cf03b51da272">CWPSTRUCT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644974(v=VS.85).aspx">CallNextHookEx</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632589(v=VS.85).aspx">Hooks</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644950(v=VS.85).aspx">SendMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644990(v=VS.85).aspx">SetWindowsHookEx</a>
 

 

