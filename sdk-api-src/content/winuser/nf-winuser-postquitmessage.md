---
UID: NF:winuser.PostQuitMessage
title: PostQuitMessage function
author: windows-sdk-content
description: Indicates to the system that a thread has made a request to terminate (quit). It is typically used in response to a WM_DESTROY message.
old-location: winmsg\postquitmessage.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\postquitmessage.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
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


Indicates to the system that a thread has made a request to terminate (quit). It is typically used in response to a <a href="https://msdn.microsoft.com/089c0645-199b-4a90-9cbc-740f0cf3267d">WM_DESTROY</a> message.


## -parameters




### -param nExitCode [in]

Type: <b>int</b>

The application exit code. This value is used as the <i>wParam</i> parameter of the <a href="https://msdn.microsoft.com/a9bff5dc-cab8-4e08-838e-d92c87c265d6">WM_QUIT</a> message.


## -returns



This function does not return a value.




## -remarks



The <b>PostQuitMessage</b> function posts a <a href="https://msdn.microsoft.com/a9bff5dc-cab8-4e08-838e-d92c87c265d6">WM_QUIT</a> message to the thread's message queue and returns immediately; the function simply indicates to the system that the thread is requesting to quit at some time in the future. 

When the thread retrieves the <a href="https://msdn.microsoft.com/a9bff5dc-cab8-4e08-838e-d92c87c265d6">WM_QUIT</a> message from its message queue, it should exit its message loop and return control to the system. The exit value returned to the system must be the <i>wParam</i> parameter of the <b>WM_QUIT</b> message. 


#### Examples

For an example, see <a href="using_messages_and_message_queues.htm">Posting a Message</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e92266a7-86ac-43f4-b0eb-762e145a1017">GetMessage</a>



<a href="https://msdn.microsoft.com/885bb607-3ec0-4e24-9f55-fbdfb1c538a1">Messages and Message Queues</a>



<a href="https://msdn.microsoft.com/b9f5baa4-8166-4d6e-b416-df023aed9bad">PeekMessage</a>



<a href="https://msdn.microsoft.com/5357de37-1e44-4e4a-bdae-b5a386032dd4">PostMessage</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/089c0645-199b-4a90-9cbc-740f0cf3267d">WM_DESTROY</a>



<a href="https://msdn.microsoft.com/a9bff5dc-cab8-4e08-838e-d92c87c265d6">WM_QUIT</a>
 

 

