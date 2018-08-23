---
UID: NF:winuser.InSendMessageEx
title: InSendMessageEx function
author: windows-sdk-content
description: Determines whether the current window procedure is processing a message that was sent from another thread (in the same process or a different process).
old-location: winmsg\insendmessageex.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\insendmessageex.htm
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: InSendMessageEx, InSendMessageEx function [Windows and Messages], _win32_InSendMessageEx, _win32_insendmessageex_cpp, winmsg.insendmessageex, winui._win32_insendmessageex, winuser/InSendMessageEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-message-l1-1-0.dll
 - Ext-MS-Win-NTUser-message-l1-1-1.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - Ext-MS-Win-NTUser-Message-l1-1-2.dll
 - Ext-MS-Win-NTUser-Message-L1-1-3.dll
api_name:
 - InSendMessageEx
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# InSendMessageEx function


## -description


Determines whether the current window procedure is processing a message that was sent from another thread (in the same process or a different process).


## -parameters




### -param lpReserved

Type: <b>LPVOID</b>

Reserved; must be <b>NULL</b>.


## -returns



Type: <strong>Type: <b>DWORD</b>
</strong>

If the message was not sent, the return value is <b>ISMEX_NOSEND</b> (0x00000000). Otherwise, the return value is one or more of the following values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ISMEX_CALLBACK</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The message was sent using the <a href="https://msdn.microsoft.com/en-us/library/ms644951(v=VS.85).aspx">SendMessageCallback</a> function. The thread that sent the message is not blocked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ISMEX_NOTIFY</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The message was sent using the <a href="https://msdn.microsoft.com/en-us/library/ms644953(v=VS.85).aspx">SendNotifyMessage</a> function. The thread that sent the message is not blocked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ISMEX_REPLIED</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The window procedure has processed the message. The thread that sent the message is no longer blocked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ISMEX_SEND</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The message was sent using the <a href="https://msdn.microsoft.com/en-us/library/ms644950(v=VS.85).aspx">SendMessage</a> or <a href="https://msdn.microsoft.com/en-us/library/ms644952(v=VS.85).aspx">SendMessageTimeout</a> function. If <b>ISMEX_REPLIED</b> is not set, the thread that sent the message is blocked.

</td>
</tr>
</table>
 




## -remarks



To determine if the sender is blocked, use the following test:

<code>fBlocked = ( InSendMessageEx(NULL) &amp; (ISMEX_REPLIED|ISMEX_SEND) ) == ISMEX_SEND;</code>




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632590(v=VS.85).aspx">Messages and Message Queues</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644950(v=VS.85).aspx">SendMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644951(v=VS.85).aspx">SendMessageCallback</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644952(v=VS.85).aspx">SendMessageTimeout</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644953(v=VS.85).aspx">SendNotifyMessage</a>
 

 

