---
UID: NF:winuser.InSendMessageEx
title: InSendMessageEx function (winuser.h)
description: Determines whether the current window procedure is processing a message that was sent from another thread (in the same process or a different process).
helpviewer_keywords: ["InSendMessageEx","InSendMessageEx function [Windows and Messages]","_win32_InSendMessageEx","_win32_insendmessageex_cpp","winmsg.insendmessageex","winui._win32_insendmessageex","winuser/InSendMessageEx"]
old-location: winmsg\insendmessageex.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\insendmessageex.htm
ms.date: 12/05/2018
ms.keywords: InSendMessageEx, InSendMessageEx function [Windows and Messages], _win32_InSendMessageEx, _win32_insendmessageex_cpp, winmsg.insendmessageex, winui._win32_insendmessageex, winuser/InSendMessageEx
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InSendMessageEx
 - winuser/InSendMessageEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-window-ext-l1-1-1.dll
 - ext-ms-win-rtcore-ntuser-message-l1-1-0.dll
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
req.apiset: ext-ms-win-ntuser-message-l1-1-0 (introduced in Windows 8)
---

# InSendMessageEx function


## -description

Determines whether the current window procedure is processing a message that was sent from another thread (in the same process or a different process).

## -parameters

### -param lpReserved

Type: <b>LPVOID</b>

Reserved; must be <b>NULL</b>.

## -returns

Type: <b>DWORD</b>

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
The message was sent using the <a href="/windows/desktop/api/winuser/nf-winuser-sendmessagecallbacka">SendMessageCallback</a> function. The thread that sent the message is not blocked.

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
The message was sent using the <a href="/windows/desktop/api/winuser/nf-winuser-sendnotifymessagea">SendNotifyMessage</a> function. The thread that sent the message is not blocked.

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
The message was sent using the <a href="/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a> or <a href="/windows/desktop/api/winuser/nf-winuser-sendmessagetimeouta">SendMessageTimeout</a> function. If <b>ISMEX_REPLIED</b> is not set, the thread that sent the message is blocked.

</td>
</tr>
</table>

## -remarks

To determine if the sender is blocked, use the following test:

<code>fBlocked = ( InSendMessageEx(NULL) &amp; (ISMEX_REPLIED|ISMEX_SEND) ) == ISMEX_SEND;</code>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/winmsg/messages-and-message-queues">Messages and Message Queues</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a>



<a href="/windows/desktop/api/winuser/nf-winuser-sendmessagecallbacka">SendMessageCallback</a>



<a href="/windows/desktop/api/winuser/nf-winuser-sendmessagetimeouta">SendMessageTimeout</a>



<a href="/windows/desktop/api/winuser/nf-winuser-sendnotifymessagea">SendNotifyMessage</a>
