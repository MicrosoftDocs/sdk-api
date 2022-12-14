---
UID: NF:winuser.GetQueueStatus
title: GetQueueStatus function (winuser.h)
description: Retrieves the type of messages found in the calling thread's message queue.
helpviewer_keywords: ["GetQueueStatus","GetQueueStatus function [Windows and Messages]","QS_ALLEVENTS","QS_ALLINPUT","QS_ALLPOSTMESSAGE","QS_HOTKEY","QS_INPUT","QS_KEY","QS_MOUSE","QS_MOUSEBUTTON","QS_MOUSEMOVE","QS_PAINT","QS_POSTMESSAGE","QS_RAWINPUT","QS_SENDMESSAGE","QS_TIMER","_win32_GetQueueStatus","_win32_getqueuestatus_cpp","winmsg.getqueuestatus","winui._win32_getqueuestatus","winuser/GetQueueStatus"]
old-location: winmsg\getqueuestatus.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\getqueuestatus.htm
ms.date: 12/05/2018
ms.keywords: GetQueueStatus, GetQueueStatus function [Windows and Messages], QS_ALLEVENTS, QS_ALLINPUT, QS_ALLPOSTMESSAGE, QS_HOTKEY, QS_INPUT, QS_KEY, QS_MOUSE, QS_MOUSEBUTTON, QS_MOUSEMOVE, QS_PAINT, QS_POSTMESSAGE, QS_RAWINPUT, QS_SENDMESSAGE, QS_TIMER, _win32_GetQueueStatus, _win32_getqueuestatus_cpp, winmsg.getqueuestatus, winui._win32_getqueuestatus, winuser/GetQueueStatus
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
 - GetQueueStatus
 - winuser/GetQueueStatus
dev_langs:
 - c++
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
 - GetQueueStatus
req.apiset: ext-ms-win-ntuser-message-l1-1-0 (introduced in Windows 8)
---

# GetQueueStatus function


## -description

Retrieves the type of messages found in the calling thread's message queue.

## -parameters

### -param flags [in]

Type: <b>UINT</b>

The types of messages for which to check. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="QS_ALLEVENTS"></a><a id="qs_allevents"></a><dl>
<dt><b>QS_ALLEVENTS</b></dt>
<dt>(QS_INPUT | QS_POSTMESSAGE | QS_TIMER | QS_PAINT | QS_HOTKEY)</dt>
</dl>
</td>
<td width="60%">
An input, <a href="/windows/desktop/winmsg/wm-timer">WM_TIMER</a>, <a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a>, <a href="/windows/desktop/inputdev/wm-hotkey">WM_HOTKEY</a>, or posted message is in the queue.

</td>
</tr>
<tr>
<td width="40%"><a id="QS_ALLINPUT"></a><a id="qs_allinput"></a><dl>
<dt><b>QS_ALLINPUT</b></dt>
<dt>(QS_INPUT | QS_POSTMESSAGE | QS_TIMER | QS_PAINT | QS_HOTKEY | QS_SENDMESSAGE)</dt>
</dl>
</td>
<td width="60%">
Any message is in the queue.

</td>
</tr>
<tr>
<td width="40%"><a id="QS_ALLPOSTMESSAGE"></a><a id="qs_allpostmessage"></a><dl>
<dt><b>QS_ALLPOSTMESSAGE</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
A posted message (other than those listed here) is in the queue.

</td>
</tr>
<tr>
<td width="40%"><a id="QS_HOTKEY"></a><a id="qs_hotkey"></a><dl>
<dt><b>QS_HOTKEY</b></dt>
<dt>0x0080</dt>
</dl>
</td>
<td width="60%">
A <a href="/windows/desktop/inputdev/wm-hotkey">WM_HOTKEY</a> message is in the queue.

</td>
</tr>
<tr>
<td width="40%"><a id="QS_INPUT"></a><a id="qs_input"></a><dl>
<dt><b>QS_INPUT</b></dt>
<dt>(QS_MOUSE | QS_KEY | QS_RAWINPUT)</dt>
</dl>
</td>
<td width="60%">
An input message is in the queue.

</td>
</tr>
<tr>
<td width="40%"><a id="QS_KEY"></a><a id="qs_key"></a><dl>
<dt><b>QS_KEY</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
A <a href="/windows/desktop/inputdev/wm-keyup">WM_KEYUP</a>, <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a>, <a href="/windows/desktop/inputdev/wm-syskeyup">WM_SYSKEYUP</a>, or <a href="/windows/desktop/inputdev/wm-syskeydown">WM_SYSKEYDOWN</a> message is in the queue.

</td>
</tr>
<tr>
<td width="40%"><a id="QS_MOUSE"></a><a id="qs_mouse"></a><dl>
<dt><b>QS_MOUSE</b></dt>
<dt>(QS_MOUSEMOVE | QS_MOUSEBUTTON)</dt>
</dl>
</td>
<td width="60%">
A <a href="/windows/desktop/inputdev/wm-mousemove">WM_MOUSEMOVE</a> message or mouse-button message (<a href="/windows/desktop/inputdev/wm-lbuttonup">WM_LBUTTONUP</a>, <a href="/windows/desktop/inputdev/wm-rbuttondown">WM_RBUTTONDOWN</a>, and so on).

</td>
</tr>
<tr>
<td width="40%"><a id="QS_MOUSEBUTTON"></a><a id="qs_mousebutton"></a><dl>
<dt><b>QS_MOUSEBUTTON</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
A mouse-button message (<a href="/windows/desktop/inputdev/wm-lbuttonup">WM_LBUTTONUP</a>, <a href="/windows/desktop/inputdev/wm-rbuttondown">WM_RBUTTONDOWN</a>, and so on).

</td>
</tr>
<tr>
<td width="40%"><a id="QS_MOUSEMOVE"></a><a id="qs_mousemove"></a><dl>
<dt><b>QS_MOUSEMOVE</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
A <a href="/windows/desktop/inputdev/wm-mousemove">WM_MOUSEMOVE</a> message is in the queue.

</td>
</tr>
<tr>
<td width="40%"><a id="QS_PAINT"></a><a id="qs_paint"></a><dl>
<dt><b>QS_PAINT</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
A <a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a> message is in the queue.

</td>
</tr>
<tr>
<td width="40%"><a id="QS_POSTMESSAGE"></a><a id="qs_postmessage"></a><dl>
<dt><b>QS_POSTMESSAGE</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
A posted message (other than those listed here) is in the queue.

</td>
</tr>
<tr>
<td width="40%"><a id="QS_RAWINPUT"></a><a id="qs_rawinput"></a><dl>
<dt><b>QS_RAWINPUT</b></dt>
<dt>0x0400</dt>
</dl>
</td>
<td width="60%">
A raw input message is in the queue. For more information, see <a href="/windows/desktop/inputdev/raw-input">Raw Input</a>.

<b>Windows 2000:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="QS_SENDMESSAGE"></a><a id="qs_sendmessage"></a><dl>
<dt><b>QS_SENDMESSAGE</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
A message sent by another thread or application is in the queue.

</td>
</tr>
<tr>
<td width="40%"><a id="QS_TIMER"></a><a id="qs_timer"></a><dl>
<dt><b>QS_TIMER</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
A <a href="/windows/desktop/winmsg/wm-timer">WM_TIMER</a> message is in the queue.

</td>
</tr>
</table>

## -returns

Type: <b>DWORD</b>

The high-order word of the return value indicates the types of messages currently in the queue. The low-order word indicates the types of messages that have been added to the queue and that are still in the queue since the last call to the <b>GetQueueStatus</b>, <a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>, or <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> function.

## -remarks

The presence of a QS_ flag in the return value does not guarantee that a subsequent call to the <a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a> or <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> function will return a message. <b>GetMessage</b> and <b>PeekMessage</b> perform some internal filtering that may cause the message to be processed internally. For this reason, the return value from <b>GetQueueStatus</b> should be considered only a hint as to whether <b>GetMessage</b> or <b>PeekMessage</b> should be called. 

The <b>QS_ALLPOSTMESSAGE</b> and <b>QS_POSTMESSAGE</b> flags differ in when they are cleared. <b>QS_POSTMESSAGE</b> is cleared when you call <a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a> or <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>, whether or not you are filtering messages. <b>QS_ALLPOSTMESSAGE</b> is cleared when you call <b>GetMessage</b> or <b>PeekMessage</b> without filtering messages (<i>wMsgFilterMin</i> and <i>wMsgFilterMax</i> are 0). This can be useful when you call <b>PeekMessage</b> multiple times to get messages in different ranges.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getinputstate">GetInputState</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>



<a href="/windows/desktop/winmsg/messages-and-message-queues">Messages and Message Queues</a>



<a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>



<b>Reference</b>
