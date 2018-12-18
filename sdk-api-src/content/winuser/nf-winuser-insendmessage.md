---
UID: NF:winuser.InSendMessage
title: InSendMessage function
author: windows-sdk-content
description: Determines whether the current window procedure is processing a message that was sent from another thread (in the same process or a different process) by a call to the SendMessage function.
old-location: winmsg\insendmessage.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\insendmessage.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: InSendMessage, InSendMessage function [Windows and Messages], _win32_InSendMessage, _win32_insendmessage_cpp, winmsg.insendmessage, winui._win32_insendmessage, winuser/InSendMessage
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
 - InSendMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InSendMessage function


## -description


Determines whether the current window procedure is processing a message that was sent from another thread (in the same process or a different process) by a call to the <a href="https://msdn.microsoft.com/en-us/library/ms644950(v=VS.85).aspx">SendMessage</a> function.

To obtain additional information about how the message was sent, use the <a href="https://msdn.microsoft.com/en-us/library/ms644942(v=VS.85).aspx">InSendMessageEx</a> function.


## -parameters






## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the window procedure is processing a message sent to it from another thread using the <a href="https://msdn.microsoft.com/en-us/library/ms644950(v=VS.85).aspx">SendMessage</a> function, the return value is nonzero.

If the window procedure is not processing a message sent to it from another thread using the <a href="https://msdn.microsoft.com/en-us/library/ms644950(v=VS.85).aspx">SendMessage</a> function, the return value is zero. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644942(v=VS.85).aspx">InSendMessageEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632590(v=VS.85).aspx">Messages and Message Queues</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644950(v=VS.85).aspx">SendMessage</a>
 

 

