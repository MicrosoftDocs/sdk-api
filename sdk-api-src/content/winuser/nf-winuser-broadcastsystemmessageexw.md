---
UID: NF:winuser.BroadcastSystemMessageExW
title: BroadcastSystemMessageExW function (winuser.h)
description: Sends a message to the specified recipients. (BroadcastSystemMessageExW)
helpviewer_keywords: ["BSF_ALLOWSFW", "BSF_FLUSHDISK", "BSF_FORCEIFHUNG", "BSF_IGNORECURRENTTASK", "BSF_LUID", "BSF_NOHANG", "BSF_NOTIMEOUTIFNOTHUNG", "BSF_POSTMESSAGE", "BSF_QUERY", "BSF_RETURNHDESK", "BSF_SENDNOTIFYMESSAGE", "BSM_ALLCOMPONENTS", "BSM_ALLDESKTOPS", "BSM_APPLICATIONS", "BroadcastSystemMessageEx", "BroadcastSystemMessageEx function [Windows and Messages]", "BroadcastSystemMessageExW", "_win32_BroadcastSystemMessageEx", "_win32_broadcastsystemmessageex_cpp", "winmsg.broadcastsystemmessageex", "winui._win32_broadcastsystemmessageex", "winuser/BroadcastSystemMessageEx", "winuser/BroadcastSystemMessageExW"]
old-location: winmsg\broadcastsystemmessageex.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\broadcastsystemmessageex.htm
ms.date: 12/05/2018
ms.keywords: BSF_ALLOWSFW, BSF_FLUSHDISK, BSF_FORCEIFHUNG, BSF_IGNORECURRENTTASK, BSF_LUID, BSF_NOHANG, BSF_NOTIMEOUTIFNOTHUNG, BSF_POSTMESSAGE, BSF_QUERY, BSF_RETURNHDESK, BSF_SENDNOTIFYMESSAGE, BSM_ALLCOMPONENTS, BSM_ALLDESKTOPS, BSM_APPLICATIONS, BroadcastSystemMessageEx, BroadcastSystemMessageEx function [Windows and Messages], BroadcastSystemMessageExA, BroadcastSystemMessageExW, _win32_BroadcastSystemMessageEx, _win32_broadcastsystemmessageex_cpp, winmsg.broadcastsystemmessageex, winui._win32_broadcastsystemmessageex, winuser/BroadcastSystemMessageEx, winuser/BroadcastSystemMessageExA, winuser/BroadcastSystemMessageExW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: BroadcastSystemMessageExW (Unicode) and BroadcastSystemMessageExA (ANSI)
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
 - BroadcastSystemMessageExW
 - winuser/BroadcastSystemMessageExW
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
 - BroadcastSystemMessageEx
 - BroadcastSystemMessageExA
 - BroadcastSystemMessageExW
---

# BroadcastSystemMessageExW function


## -description

Sends a message to the specified recipients. The recipients can be applications, installable drivers, network drivers, system-level device drivers, or any combination of these system components. 
			
            

This function is similar to <a href="/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage">BroadcastSystemMessage</a> except that this function can return more information from the recipients.

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
<td width="40%"><a id="BSF_LUID"></a><a id="bsf_luid"></a><dl>
<dt><b>BSF_LUID</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
 If <b>BSF_LUID</b> is set, the message is sent to the window that has the same LUID as specified in the <b>luid</b> member of the <a href="/windows/desktop/api/winuser/ns-winuser-bsminfo">BSMINFO</a> structure.

<b>Windows 2000:  </b>This flag is not supported.

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
<td width="40%"><a id="BSF_RETURNHDESK"></a><a id="bsf_returnhdesk"></a><dl>
<dt><b>BSF_RETURNHDESK</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
 If access is denied and both this and <b>BSF_QUERY</b> are set, <a href="/windows/desktop/api/winuser/ns-winuser-bsminfo">BSMINFO</a> returns both the desktop handle and the window handle. If access is denied and only <b>BSF_QUERY</b> is set, only the window handle is returned by <b>BSMINFO</b>.

<b>Windows 2000:  </b>This flag is not supported.

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

### -param pbsmInfo [out, optional]

Type: <b>PBSMINFO</b>

A pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-bsminfo">BSMINFO</a> structure that contains additional information if the request is denied and <i>dwFlags</i> is set to <b>BSF_QUERY</b>.

## -returns

Type: <b>long</b>

If the function succeeds, the return value is a positive value.

If the function is unable to broadcast the message, the return value is –1. 

If the <i>dwFlags</i> parameter is <b>BSF_QUERY</b> and at least one recipient returned <b>BROADCAST_QUERY_DENY</b> to the corresponding message, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If <b>BSF_QUERY</b> is not specified, the function sends the specified message to all requested recipients, ignoring values returned by those recipients.

If the caller's thread is on a desktop other than that of the window that denied the request, the caller must call <a href="/windows/desktop/api/winuser/nf-winuser-setthreaddesktop">SetThreadDesktop</a><b>(hdesk)</b> to query anything on that window. Also, the caller must call <a href="/windows/desktop/api/winuser/nf-winuser-closedesktop">CloseDesktop</a> on the returned <b>hdesk</b> handle.

The system only does marshalling for system messages (those in the range 0 to (<a href="/windows/desktop/winmsg/wm-user">WM_USER</a>-1)). To send other messages (those &gt;= <b>WM_USER</b>) to another process, you must do custom marshalling.





> [!NOTE]
> The winuser.h header defines BroadcastSystemMessageEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winuser/ns-winuser-bsminfo">BSMINFO</a>



<a href="/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage">BroadcastSystemMessage</a>



<b>Conceptual</b>



<a href="/windows/desktop/winmsg/messages-and-message-queues">Messages and Message Queues</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-sendnotifymessagea">SendNotifyMessage</a>
