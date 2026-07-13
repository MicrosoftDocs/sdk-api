---
UID: NF:winuser.BroadcastSystemMessageW
title: BroadcastSystemMessageW function (winuser.h)
description: The BroadcastSystemMessageW (Unicode) function sends a message to the specified recipients. (BroadcastSystemMessageW)
helpviewer_keywords: ["BSF_ALLOWSFW", "BSF_FLUSHDISK", "BSF_FORCEIFHUNG", "BSF_IGNORECURRENTTASK", "BSF_NOHANG", "BSF_NOTIMEOUTIFNOTHUNG", "BSF_POSTMESSAGE", "BSF_QUERY", "BSF_SENDNOTIFYMESSAGE", "BSM_ALLCOMPONENTS", "BSM_ALLDESKTOPS", "BSM_APPLICATIONS", "BroadcastSystemMessage", "BroadcastSystemMessage function [Windows and Messages]", "BroadcastSystemMessageW", "_win32_BroadcastSystemMessage", "_win32_broadcastsystemmessage_cpp", "winmsg.broadcastsystemmessage", "winui._win32_broadcastsystemmessage", "winuser/BroadcastSystemMessage", "winuser/BroadcastSystemMessageW"]
old-location: winmsg\broadcastsystemmessage.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\broadcastsystemmessage.htm
ms.date: 08/02/2022
ms.keywords: BSF_ALLOWSFW, BSF_FLUSHDISK, BSF_FORCEIFHUNG, BSF_IGNORECURRENTTASK, BSF_NOHANG, BSF_NOTIMEOUTIFNOTHUNG, BSF_POSTMESSAGE, BSF_QUERY, BSF_SENDNOTIFYMESSAGE, BSM_ALLCOMPONENTS, BSM_ALLDESKTOPS, BSM_APPLICATIONS, BroadcastSystemMessage, BroadcastSystemMessage function [Windows and Messages], BroadcastSystemMessageW, _win32_BroadcastSystemMessage, _win32_broadcastsystemmessage_cpp, winmsg.broadcastsystemmessage, winui._win32_broadcastsystemmessage, winuser/BroadcastSystemMessage, winuser/BroadcastSystemMessageW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: BroadcastSystemMessageW (Unicode)
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
 - BroadcastSystemMessageW
 - winuser/BroadcastSystemMessageW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - BroadcastSystemMessage
 - BroadcastSystemMessageW
---

# BroadcastSystemMessageW function


## -description

Sends a message to the specified recipients. The recipients can be applications, installable drivers, network drivers, system-level device drivers, or any combination of these system components. 

			

To receive additional information if the request is defined, use the <a href="/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessageexa">BroadcastSystemMessageEx</a> function.

## -parameters

### -param flags [in]

Type: <b>DWORD</b>

The broadcast option. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BSF_ALLOWSFW"></a><a id="bsf_allowsfw"></a><dl>
<dt><b>BSF_ALLOWSFW</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
 Enables the recipient to set the foreground window while processing the message.

</td>
</tr>
<tr>
<td width="40%"><a id="BSF_FLUSHDISK"></a><a id="bsf_flushdisk"></a><dl>
<dt><b>BSF_FLUSHDISK</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Flushes the disk after each recipient processes the message.

</td>
</tr>
<tr>
<td width="40%"><a id="BSF_FORCEIFHUNG"></a><a id="bsf_forceifhung"></a><dl>
<dt><b>BSF_FORCEIFHUNG</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Continues to broadcast the message, even if the time-out period elapses or one of the recipients is not responding.

</td>
</tr>
<tr>
<td width="40%"><a id="BSF_IGNORECURRENTTASK"></a><a id="bsf_ignorecurrenttask"></a><dl>
<dt><b>BSF_IGNORECURRENTTASK</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Does not send the message to windows that belong to the current task. This prevents an application from receiving its own message.

</td>
</tr>
<tr>
<td width="40%"><a id="BSF_NOHANG"></a><a id="bsf_nohang"></a><dl>
<dt><b>BSF_NOHANG</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Forces a nonresponsive application to time out. If one of the recipients times out, do not continue broadcasting the message.

</td>
</tr>
<tr>
<td width="40%"><a id="BSF_NOTIMEOUTIFNOTHUNG"></a><a id="bsf_notimeoutifnothung"></a><dl>
<dt><b>BSF_NOTIMEOUTIFNOTHUNG</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Waits for a response to the message, as long as the recipient is not being unresponsive. Does not time out.

</td>
</tr>
<tr>
<td width="40%"><a id="BSF_POSTMESSAGE"></a><a id="bsf_postmessage"></a><dl>
<dt><b>BSF_POSTMESSAGE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Posts the message. Do not use in combination with <b>BSF_QUERY</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="BSF_QUERY"></a><a id="bsf_query"></a><dl>
<dt><b>BSF_QUERY</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Sends the message to one recipient at a time, sending to a subsequent recipient only if the current recipient returns <b>TRUE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="BSF_SENDNOTIFYMESSAGE"></a><a id="bsf_sendnotifymessage"></a><dl>
<dt><b>BSF_SENDNOTIFYMESSAGE</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
 Sends the message using <a href="/windows/desktop/api/winuser/nf-winuser-sendnotifymessagea">SendNotifyMessage</a> function. Do not use in combination with <b>BSF_QUERY</b>.

</td>
</tr>
</table>

### -param lpInfo [in, out, optional]

Type: <b>LPDWORD</b>

A pointer to a variable that contains and receives information about the recipients of the message. 
                    

When the function returns, this variable receives a combination of these values identifying which recipients actually received the message. 

If this parameter is <b>NULL</b>, the function broadcasts to all components. 

This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BSM_ALLCOMPONENTS"></a><a id="bsm_allcomponents"></a><dl>
<dt><b>BSM_ALLCOMPONENTS</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Broadcast to all system components.

</td>
</tr>
<tr>
<td width="40%"><a id="BSM_ALLDESKTOPS"></a><a id="bsm_alldesktops"></a><dl>
<dt><b>BSM_ALLDESKTOPS</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
 Broadcast to all desktops. Requires the <a href="/windows/desktop/SecAuthZ/authorization-constants">SE_TCB_NAME</a> privilege.

</td>
</tr>
<tr>
<td width="40%"><a id="BSM_APPLICATIONS"></a><a id="bsm_applications"></a><dl>
<dt><b>BSM_APPLICATIONS</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Broadcast to applications.

</td>
</tr>
</table>

### -param Msg [in]

Type: <b>UINT</b>

The message to be sent. 

For lists of the system-provided messages, see <a href="/windows/desktop/winmsg/about-messages-and-message-queues">System-Defined Messages</a>.

### -param wParam [in]

Type: <b>WPARAM</b>

Additional message-specific information.

### -param lParam [in]

Type: <b>LPARAM</b>

Additional message-specific information.

## -returns

Type: <b>long</b>

If the function succeeds, the return value is a positive value.

If the function is unable to broadcast the message, the return value is –1. 

If the <i>dwFlags</i> parameter is <b>BSF_QUERY</b> and at least one recipient returned <b>BROADCAST_QUERY_DENY</b> to the corresponding message, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If <b>BSF_QUERY</b> is not specified, the function sends the specified message to all requested recipients, ignoring values returned by those recipients.

The system only does marshalling for system messages (those in the range 0 to (<a href="/windows/desktop/winmsg/wm-user">WM_USER</a>-1)). To send other messages (those &gt;= <b>WM_USER</b>) to another process, you must do custom marshalling.


#### Examples

For an example, see <a href="/windows/desktop/ProcThread/terminating-a-process">Terminating a Process</a>.

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines BroadcastSystemMessage as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessageexa">BroadcastSystemMessageEx</a>



<b>Conceptual</b>



<a href="/windows/desktop/winmsg/messages-and-message-queues">Messages and Message Queues</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-sendnotifymessagea">SendNotifyMessage</a>
