---
UID: NF:winuser.PostQuitMessage
title: PostQuitMessage function
author: windows-sdk-content
description: Indicates to the system that a thread has made a request to terminate (quit). It is typically used in response to a WM_DESTROY message.
old-location: winmsg\postquitmessage.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\postquitmessage.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PostQuitMessage, PostQuitMessage function [Windows and Messages], _win32_PostQuitMessage, _win32_postquitmessage_cpp, winmsg.postquitmessage, winui._win32_postquitmessage, winuser/PostQuitMessage
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
 - API-MS-Win-NTUser-IE-message-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-message-l1-1-0.dll
 - Ext-MS-Win-NTUser-message-l1-1-1.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - Ext-MS-Win-NTUser-Message-l1-1-2.dll
 - Ext-MS-Win-NTUser-Message-L1-1-3.dll
api_name:
 - PostQuitMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PostQuitMessage function


## -description


Indicates to the system that a thread has made a request to terminate (quit). It is typically used in response to a <a href="https://msdn.microsoft.com/en-us/library/ms632620(v=VS.85).aspx">WM_DESTROY</a> message.


## -parameters




### -param nExitCode [in]

Type: <b>int</b>

The application exit code. This value is used as the <i>wParam</i> parameter of the <a href="https://msdn.microsoft.com/en-us/library/ms632641(v=VS.85).aspx">WM_QUIT</a> message.


## -returns



This function does not return a value.




## -remarks



The <b>PostQuitMessage</b> function posts a <a href="https://msdn.microsoft.com/en-us/library/ms632641(v=VS.85).aspx">WM_QUIT</a> message to the thread's message queue and returns immediately; the function simply indicates to the system that the thread is requesting to quit at some time in the future. 

When the thread retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms632641(v=VS.85).aspx">WM_QUIT</a> message from its message queue, it should exit its message loop and return control to the system. The exit value returned to the system must be the <i>wParam</i> parameter of the <b>WM_QUIT</b> message. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms644928(v=VS.85).aspx">Posting a Message</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644936(v=VS.85).aspx">GetMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632590(v=VS.85).aspx">Messages and Message Queues</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644943(v=VS.85).aspx">PeekMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644944(v=VS.85).aspx">PostMessage</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632620(v=VS.85).aspx">WM_DESTROY</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632641(v=VS.85).aspx">WM_QUIT</a>
 

 

