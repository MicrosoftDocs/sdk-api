---
UID: NF:winuser.GetInputState
title: GetInputState function
author: windows-sdk-content
description: Determines whether there are mouse-button or keyboard messages in the calling thread's message queue.
old-location: winmsg\getinputstate.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\getinputstate.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetInputState, GetInputState function [Windows and Messages], _win32_GetInputState, _win32_getinputstate_cpp, winmsg.getinputstate, winui._win32_getinputstate, winuser/GetInputState
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
api_name:
 - GetInputState
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetInputState function


## -description


Determines whether there are mouse-button or keyboard messages in the calling thread's message queue. 


## -parameters






## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the queue contains one or more new mouse-button or keyboard messages, the return value is nonzero.

If there are no new mouse-button or keyboard messages in the queue, the return value is zero. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644940(v=VS.85).aspx">GetQueueStatus</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632590(v=VS.85).aspx">Messages and Message Queues</a>



<b>Reference</b>
 

 

