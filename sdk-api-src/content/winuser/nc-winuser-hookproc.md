---
UID: NC:winuser.HOOKPROC
title: HOOKPROC
author: windows-sdk-content
description: An application-defined or library-defined callback function used with the SetWindowsHookEx function. The system calls this function after the SendMessage function is called. The hook procedure can examine the message; it cannot modify it.
old-location: winmsg\callwndretproc.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookfunctions\callwndretproc.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: CallWndRetProc, CallWndRetProc callback, CallWndRetProc callback function [Windows and Messages], HOOKPROC, _win32_CallWndRetProc, _win32_callwndretproc_cpp, winmsg.callwndretproc, winui._win32_callwndretproc, winuser/CallWndRetProc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winuser.h
api_name:
 - CallWndRetProc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# HOOKPROC callback function


## -description


An application-defined or library-defined callback function used with the <a href="https://msdn.microsoft.com/66c96282-528c-4f57-acab-ae03178e4fe9">SetWindowsHookEx</a> function. The system calls this function after the <a href="https://msdn.microsoft.com/c069c542-f854-41ff-a523-90f3855e2277">SendMessage</a> function is called. The hook procedure can examine the message; it cannot modify it.

The <b>HOOKPROC</b> type defines a pointer to this callback function. <i>CallWndRetProc</i> is a placeholder for the application-defined or library-defined function name.


## -parameters




### -param code


### -param wParam [in]

Type: <b>WPARAM</b>

Specifies whether the message is sent by the current process. If the message is sent by the current process, it is nonzero; otherwise, it is <b>NULL</b>. 


### -param lParam [in]

Type: <b>LPARAM</b>

A pointer to a <a href="https://msdn.microsoft.com/e3e8e573-870d-4d8a-b55b-88d58910c384">CWPRETSTRUCT</a> structure that contains details about the message. 


#### - nCode [in]

Type: <b>int</b>

Specifies whether the hook procedure must process the message. If <i>nCode</i> is <b>HC_ACTION</b>, the hook procedure must process the message. If 	<i>nCode</i> is less than zero, the hook procedure must pass the message to the <a href="https://msdn.microsoft.com/2f734ea7-7724-46be-99a0-2bfa27b2ed99">CallNextHookEx</a> function without further processing and should return the value returned by <b>CallNextHookEx</b>. 


## -returns



Type: <strong>Type: <b>LRESULT</b>
</strong>

If <i>nCode</i> is less than zero, the hook procedure must return the value returned by <a href="https://msdn.microsoft.com/2f734ea7-7724-46be-99a0-2bfa27b2ed99">CallNextHookEx</a>. 

If <i>nCode</i> is greater than or equal to zero, it is highly recommended that you call <a href="https://msdn.microsoft.com/2f734ea7-7724-46be-99a0-2bfa27b2ed99">CallNextHookEx</a> and return the value it returns; otherwise, other applications that have installed <a href="about_hooks.htm">WH_CALLWNDPROCRET</a> hooks will not receive hook notifications and may behave incorrectly as a result. If the hook procedure does not call <b>CallNextHookEx</b>, the return value should be zero. 




## -remarks



An application installs the hook procedure by specifying the <a href="about_hooks.htm">WH_CALLWNDPROCRET</a> hook type and a pointer to the hook procedure in a call to the <a href="https://msdn.microsoft.com/66c96282-528c-4f57-acab-ae03178e4fe9">SetWindowsHookEx</a> function. 




## -see-also




<a href="https://msdn.microsoft.com/e3e8e573-870d-4d8a-b55b-88d58910c384">CWPRETSTRUCT</a>



<a href="https://msdn.microsoft.com/2f734ea7-7724-46be-99a0-2bfa27b2ed99">CallNextHookEx</a>



<a href="https://msdn.microsoft.com/25df5ac2-f007-4683-ba89-537dc7a3c15e">CallWndProc</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/987095d7-059f-4eae-925d-6723ab6d524c">Hooks</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/c069c542-f854-41ff-a523-90f3855e2277">SendMessage</a>



<a href="https://msdn.microsoft.com/66c96282-528c-4f57-acab-ae03178e4fe9">SetWindowsHookEx</a>
 

 

