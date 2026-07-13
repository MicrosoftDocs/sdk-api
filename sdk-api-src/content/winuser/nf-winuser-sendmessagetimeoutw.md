---
UID: NF:winuser.SendMessageTimeoutW
title: SendMessageTimeoutW function (winuser.h)
description: Sends the specified message to one or more windows. (Unicode)
helpviewer_keywords: ["SMTO_ABORTIFHUNG", "SMTO_BLOCK", "SMTO_ERRORONEXIT", "SMTO_NORMAL", "SMTO_NOTIMEOUTIFNOTHUNG", "SendMessageTimeout", "SendMessageTimeout function [Windows and Messages]", "SendMessageTimeoutW", "_win32_SendMessageTimeout", "_win32_sendmessagetimeout_cpp", "winmsg.sendmessagetimeout", "winui._win32_sendmessagetimeout", "winuser/SendMessageTimeout", "winuser/SendMessageTimeoutW"]
old-location: winmsg\sendmessagetimeout.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\sendmessagetimeout.htm
ms.date: 12/05/2018
ms.keywords: SMTO_ABORTIFHUNG, SMTO_BLOCK, SMTO_ERRORONEXIT, SMTO_NORMAL, SMTO_NOTIMEOUTIFNOTHUNG, SendMessageTimeout, SendMessageTimeout function [Windows and Messages], SendMessageTimeoutA, SendMessageTimeoutW, _win32_SendMessageTimeout, _win32_sendmessagetimeout_cpp, winmsg.sendmessagetimeout, winui._win32_sendmessagetimeout, winuser/SendMessageTimeout, winuser/SendMessageTimeoutA, winuser/SendMessageTimeoutW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SendMessageTimeoutW (Unicode) and SendMessageTimeoutA (ANSI)
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
 - SendMessageTimeoutW
 - winuser/SendMessageTimeoutW
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
 - SendMessageTimeout
 - SendMessageTimeoutA
 - SendMessageTimeoutW
req.apiset: ext-ms-win-ntuser-message-l1-1-0 (introduced in Windows 8)
---

# SendMessageTimeoutW function


## -description

Sends the specified message to one or more windows.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window whose window procedure will receive the message.

If this parameter is <b>HWND_BROADCAST</b> ((HWND)0xffff), the message is sent to all top-level windows in the system, including disabled or invisible unowned windows. The function does not return until each window has timed out. Therefore, the total wait time can be up to the value of <i>uTimeout</i> multiplied by the number of top-level windows.

### -param Msg [in]

Type: <b>UINT</b>

The message to be sent.

For lists of the system-provided messages, see <a href="/windows/desktop/winmsg/about-messages-and-message-queues">System-Defined Messages</a>.

### -param wParam [in]

Type: <b>WPARAM</b>

Any additional message-specific information.

### -param lParam [in]

Type: <b>LPARAM</b>

Any additional message-specific information.

### -param fuFlags [in]

Type: <b>UINT</b>

The behavior of this function. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SMTO_ABORTIFHUNG"></a><a id="smto_abortifhung"></a><dl>
<dt><b>SMTO_ABORTIFHUNG</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The function returns without waiting for the time-out period to elapse if the receiving thread appears to not respond or "hangs."

</td>
</tr>
<tr>
<td width="40%"><a id="SMTO_BLOCK"></a><a id="smto_block"></a><dl>
<dt><b>SMTO_BLOCK</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Prevents the calling thread from processing any other requests until the function returns.

</td>
</tr>
<tr>
<td width="40%"><a id="SMTO_NORMAL"></a><a id="smto_normal"></a><dl>
<dt><b>SMTO_NORMAL</b></dt>
<dt>0x0000</dt>
</dl>
</td>
<td width="60%">
The calling thread is not prevented from processing other requests while waiting for the function to return.

</td>
</tr>
<tr>
<td width="40%"><a id="SMTO_NOTIMEOUTIFNOTHUNG"></a><a id="smto_notimeoutifnothung"></a><dl>
<dt><b>SMTO_NOTIMEOUTIFNOTHUNG</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
The function does not enforce the time-out period as long as the receiving thread is processing messages.

</td>
</tr>
<tr>
<td width="40%"><a id="SMTO_ERRORONEXIT"></a><a id="smto_erroronexit"></a><dl>
<dt><b>SMTO_ERRORONEXIT</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
The function should return 0 if the receiving window is destroyed or its owning thread dies while the message is being processed.

</td>
</tr>
</table>

### -param uTimeout [in]

Type: <b>UINT</b>

The duration of the time-out period, in milliseconds. If the message is a broadcast message, each window can use the full time-out period. For example, if you specify a five second time-out period and there are three top-level windows that fail to process the message, you could have up to a 15 second delay.

### -param lpdwResult [out, optional]

Type: <b>PDWORD_PTR</b>

The result of the message processing. The value of this parameter depends on the message that is specified.

## -returns

Type: <b>LRESULT</b>

If the function succeeds, the return value is nonzero. <b>SendMessageTimeout</b> does not provide information about individual windows timing out if <b>HWND_BROADCAST</b> is used.

If the function fails or times out, the return value is 0.
Note that the function does not always call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a>
on failure.
If the reason for failure is important to you, call SetLastError(ERROR_SUCCESS)
before calling SendMessageTimeout. If the function returns 0, and
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>
returns ERROR_SUCCESS, then treat it as a generic failure.

## -remarks

The function calls the window procedure for the specified window and, if the specified window belongs to a different thread, does not return until the window procedure has processed the message or the specified time-out period has elapsed. If the window receiving the message belongs to the same queue as the current thread, the window procedure is called directly—the time-out value is ignored.

This function considers that a thread is not responding if it has not called <a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a> or a similar function within five seconds.

The system only does marshalling for system messages (those in the range 0 to (<a href="/windows/desktop/winmsg/wm-user">WM_USER</a>-1)). To send other messages (those &gt;= <b>WM_USER</b>) to another process, you must do custom marshalling.





> [!NOTE]
> The winuser.h header defines SendMessageTimeout as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>



<a href="/windows/desktop/api/winuser/nf-winuser-insendmessage">InSendMessage</a>



<a href="/windows/desktop/winmsg/messages-and-message-queues">Messages and Message Queues</a>



<a href="/windows/desktop/api/winuser/nf-winuser-postmessagea">PostMessage</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea">SendDlgItemMessage</a>



<a href="/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a>



<a href="/windows/desktop/api/winuser/nf-winuser-sendmessagecallbacka">SendMessageCallback</a>



<a href="/windows/desktop/api/winuser/nf-winuser-sendnotifymessagea">SendNotifyMessage</a>
