---
UID: NF:winuser.InSendMessageEx
title: InSendMessageEx function
author: windows-sdk-content
description: Determines whether the current window procedure is processing a message that was sent from another thread (in the same process or a different process).
old-location: winmsg\insendmessageex.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\insendmessageex.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: InSendMessageEx, InSendMessageEx function [Windows and Messages], _win32_InSendMessageEx, _win32_insendmessageex_cpp, winmsg.insendmessageex, winui._win32_insendmessageex, winuser/InSendMessageEx
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
req.typenames: 
req.redist: 
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
The message was sent using the <a href="https://msdn.microsoft.com/6246e7ae-da06-4b86-b0d5-1743522b1bda">SendMessageCallback</a> function. The thread that sent the message is not blocked.

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
The message was sent using the <a href="https://msdn.microsoft.com/08767153-34f5-4d31-9705-5a1862b9dd10">SendNotifyMessage</a> function. The thread that sent the message is not blocked.

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
The message was sent using the <a href="https://msdn.microsoft.com/c069c542-f854-41ff-a523-90f3855e2277">SendMessage</a> or <a href="https://msdn.microsoft.com/c8096383-9fdf-42b3-af98-0bfe0d02c656">SendMessageTimeout</a> function. If <b>ISMEX_REPLIED</b> is not set, the thread that sent the message is blocked.

</td>
</tr>
</table>
 




## -remarks



To determine if the sender is blocked, use the following test:

<code>fBlocked = ( InSendMessageEx(NULL) &amp; (ISMEX_REPLIED|ISMEX_SEND) ) == ISMEX_SEND;</code>




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/885bb607-3ec0-4e24-9f55-fbdfb1c538a1">Messages and Message Queues</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/c069c542-f854-41ff-a523-90f3855e2277">SendMessage</a>



<a href="https://msdn.microsoft.com/6246e7ae-da06-4b86-b0d5-1743522b1bda">SendMessageCallback</a>



<a href="https://msdn.microsoft.com/c8096383-9fdf-42b3-af98-0bfe0d02c656">SendMessageTimeout</a>



<a href="https://msdn.microsoft.com/08767153-34f5-4d31-9705-5a1862b9dd10">SendNotifyMessage</a>
 

 

