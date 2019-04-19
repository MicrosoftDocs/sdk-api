---
UID: NF:winuser.ReplyMessage
title: ReplyMessage function (winuser.h)
author: windows-sdk-content
description: Replies to a message sent from another thread by the SendMessage function.
old-location: winmsg\replymessage.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\replymessage.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ReplyMessage, ReplyMessage function [Windows and Messages], _win32_ReplyMessage, _win32_replymessage_cpp, winmsg.replymessage, winui._win32_replymessage, winuser/ReplyMessage
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
 - Ext-MS-Win-NTUser-Message-l1-1-2.dll
 - Ext-MS-Win-NTUser-Message-L1-1-3.dll
api_name:
 - ReplyMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ReplyMessage function


## -description


Replies to a message sent from another thread by the <a href="https://msdn.microsoft.com/en-us/library/ms644950(v=VS.85).aspx">SendMessage</a> function.


## -parameters




### -param lResult [in]

Type: <b>LRESULT</b>

The result of the message processing. The possible values are based on the message sent.


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the calling thread was processing a message sent from another thread or process, the return value is nonzero.

If the calling thread was not processing a message sent from another thread or process, the return value is zero. 




## -remarks



By calling this function, the window procedure that receives the message allows the thread that called <a href="https://msdn.microsoft.com/en-us/library/ms644950(v=VS.85).aspx">SendMessage</a> to continue to run as though the thread receiving the message had returned control. The thread that calls the <b>ReplyMessage</b> function also continues to run. 

If the message was not sent through <a href="https://msdn.microsoft.com/en-us/library/ms644950(v=VS.85).aspx">SendMessage</a> or if the message was sent by the same thread, <b>ReplyMessage</b> has no effect. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms644928(v=VS.85).aspx">Sending a Message</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644941(v=VS.85).aspx">InSendMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632590(v=VS.85).aspx">Messages and Message Queues</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644950(v=VS.85).aspx">SendMessage</a>
 

 

