---
UID: NF:winuser.PeekMessageA
title: PeekMessageA function (winuser.h)
description: Dispatches incoming nonqueued messages, checks the thread message queue for a posted message, and retrieves the message (if any exist). (ANSI)
helpviewer_keywords: ["PM_NOREMOVE", "PM_NOYIELD", "PM_QS_INPUT", "PM_QS_PAINT", "PM_QS_POSTMESSAGE", "PM_QS_SENDMESSAGE", "PM_REMOVE", "PeekMessageA", "winuser/PeekMessageA"]
old-location: winmsg\peekmessage.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\peekmessage.htm
ms.date: 12/05/2018
ms.keywords: PM_NOREMOVE, PM_NOYIELD, PM_QS_INPUT, PM_QS_PAINT, PM_QS_POSTMESSAGE, PM_QS_SENDMESSAGE, PM_REMOVE, PeekMessage, PeekMessage function [Windows and Messages], PeekMessageA, PeekMessageW, _win32_PeekMessage, _win32_peekmessage_cpp, winmsg.peekmessage, winui._win32_peekmessage, winuser/PeekMessage, winuser/PeekMessageA, winuser/PeekMessageW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PeekMessageW (Unicode) and PeekMessageA (ANSI)
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
 - PeekMessageA
 - winuser/PeekMessageA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-message-ansi-l1-1-0.dll
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
 - PeekMessage
 - PeekMessageA
 - PeekMessageW
req.apiset: ext-ms-win-ntuser-message-l1-1-0 (introduced in Windows 8)
---

# PeekMessageA function


## -description

Dispatches incoming nonqueued messages, checks the thread message queue for a posted message, and retrieves the message (if any exist).

## -parameters

### -param lpMsg [out]

Type: <b>LPMSG</b>

A pointer to an <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> structure that receives message information.

### -param hWnd [in, optional]

Type: <b>HWND</b>

A handle to the window whose messages are to be retrieved. The window must belong to the current thread. 



If <i>hWnd</i> is <b>NULL</b>, <b>PeekMessage</b> retrieves messages for any window that belongs to the current thread, and any messages on the current thread's message queue whose <b>hwnd</b> value is <b>NULL</b> (see the <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> structure). Therefore if hWnd is <b>NULL</b>, both window messages and thread messages are processed.

 If <i>hWnd</i> is -1, <b>PeekMessage</b> retrieves only messages on the current thread's message queue whose <b>hwnd</b> value is <b>NULL</b>, that is, thread messages as posted by  <a href="/windows/desktop/api/winuser/nf-winuser-postmessagea">PostMessage</a> (when the <i>hWnd</i> parameter is <b>NULL</b>) or <a href="/windows/desktop/api/winuser/nf-winuser-postthreadmessagea">PostThreadMessage</a>.

### -param wMsgFilterMin [in]

Type: <b>UINT</b>

The value of the first message in the range of messages to be examined. Use <b>WM_KEYFIRST</b> (0x0100) to specify the first keyboard message or <b>WM_MOUSEFIRST</b> (0x0200) to specify the first mouse message.

If <i>wMsgFilterMin</i> and <i>wMsgFilterMax</i> are both zero, <b>PeekMessage</b> returns all available messages (that is, no range filtering is performed).

### -param wMsgFilterMax [in]

Type: <b>UINT</b>

The value of the last message in the range of messages to be examined. Use <b>WM_KEYLAST</b> to specify the last keyboard message or <b>WM_MOUSELAST</b> to specify the last mouse message.

If <i>wMsgFilterMin</i> and <i>wMsgFilterMax</i> are both zero, <b>PeekMessage</b> returns all available messages (that is, no range filtering is performed).

### -param wRemoveMsg [in]

Type: <b>UINT</b>

Specifies how messages are to be handled. This parameter can be one or more of the following values.

| Value | Meaning |
|-------|---------|
| **PM\_NOREMOVE**<br>`0x0000`  | Messages are not removed from the queue after processing by **PeekMessage**. |
| **PM\_REMOVE**<br>`0x0001` | Messages are removed from the queue after processing by **PeekMessage**. |
| **PM\_NOYIELD**<br>`0x0002` | Prevents the system from releasing any thread that is waiting for the caller to go idle (see [WaitForInputIdle](/windows/desktop/api/winuser/nf-winuser-waitforinputidle)). Combine this value with either **PM\_NOREMOVE** or **PM\_REMOVE**. |

By default, all message types are processed. To specify that only certain message should be processed, specify one or more of the following values.

| Value | Meaning |
|-------|---------|
| **PM\_QS\_INPUT**<br>`(QS_INPUT << 16)` | Process mouse and keyboard messages. |
| **PM\_QS\_POSTMESSAGE**<br>`((QS_POSTMESSAGE \| QS_HOTKEY \| QS_TIMER) << 16)` | Process all posted messages, including timers and hotkeys. |
| **PM\_QS\_PAINT**<br>`(QS_PAINT << 16)` | Process paint messages. |
| **PM\_QS\_SENDMESSAGE**<br>`(QS_SENDMESSAGE << 16)` | Process all sent messages. |

For more info on listed `QS_` flags and types of messages see [GetQueueStatus](nf-winuser-getqueuestatus.md) documentation.

## -returns

Type: <b>BOOL</b>

If a message is available, the return value is nonzero.

If no messages are available, the return value is zero.

## -remarks

<b>PeekMessage</b> retrieves messages associated with the window identified by the <i>hWnd</i> parameter or any of its children as specified by the <a href="/windows/desktop/api/winuser/nf-winuser-ischild">IsChild</a> function, and within the range of message values given by the <i>wMsgFilterMin</i> and <i>wMsgFilterMax</i> parameters. Note that an application can only use the low word in the <i>wMsgFilterMin</i> and <i>wMsgFilterMax</i> parameters; the high word is reserved for the system.

Note that <b>PeekMessage</b> always retrieves <a href="/windows/desktop/winmsg/wm-quit">WM_QUIT</a> messages, no matter which values you specify for <i>wMsgFilterMin</i> and <i>wMsgFilterMax</i>.

During this call, the system dispatches (<a href="/windows/win32/api/winuser/nf-winuser-dispatchmessage">DispatchMessage</a>) pending,  nonqueued messages, that is, messages sent to windows owned by the calling thread using the <a href="/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a>, <a href="/windows/desktop/api/winuser/nf-winuser-sendmessagecallbacka">SendMessageCallback</a>, <a href="/windows/desktop/api/winuser/nf-winuser-sendmessagetimeouta">SendMessageTimeout</a>, or <a href="/windows/desktop/api/winuser/nf-winuser-sendnotifymessagea">SendNotifyMessage</a> function. Then the first queued message that matches the specified filter is retrieved. The system may also process internal events. If no filter is specified, messages are processed in the following order:

<ul>
<li>Sent messages </li>
<li>Posted messages </li>
<li>Input (hardware) messages and system internal events </li>
<li>Sent messages (again) </li>
<li>
<a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a> messages </li>
<li>
<a href="/windows/desktop/winmsg/wm-timer">WM_TIMER</a> messages </li>
</ul>
To retrieve input messages before posted messages, use the <i>wMsgFilterMin</i> and <i>wMsgFilterMax</i> parameters. 

The <b>PeekMessage</b> function normally does not remove <a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a> messages from the queue. <b>WM_PAINT</b> messages remain in the queue until they are processed. However, if a <b>WM_PAINT</b> message has a <b>NULL</b> update region, <b>PeekMessage</b> does remove it from the queue.

 If a top-level window stops responding to messages for more than several seconds, the system considers the window to be not responding and replaces it with a ghost window that has the same z-order, location, size, and visual attributes. This allows the user to move it, resize it, or even close the application. However, these are the only actions available because the application is actually not responding. When an application is being debugged, the system does not generate a ghost window. 

<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. The output is in the mode of the window that the message is targeting. The calling thread is not taken into consideration.


#### Examples

For an example, see <a href="/windows/desktop/winmsg/using-messages-and-message-queues">Examining a Message Queue</a>.

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines PeekMessage as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>



<a href="/windows/desktop/api/winuser/nf-winuser-ischild">IsChild</a>



<a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a>



<a href="/windows/desktop/winmsg/messages-and-message-queues">Messages and Message Queues</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-waitforinputidle">WaitForInputIdle</a>



<a href="/windows/desktop/api/winuser/nf-winuser-waitmessage">WaitMessage</a>
