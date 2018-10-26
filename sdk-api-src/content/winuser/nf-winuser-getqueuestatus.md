---
UID: NF:winuser.GetQueueStatus
title: GetQueueStatus function
author: windows-sdk-content
description: Retrieves the type of messages found in the calling thread's message queue.
old-location: winmsg\getqueuestatus.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\getqueuestatus.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetQueueStatus, GetQueueStatus function [Windows and Messages], QS_ALLEVENTS, QS_ALLINPUT, QS_ALLPOSTMESSAGE, QS_HOTKEY, QS_INPUT, QS_KEY, QS_MOUSE, QS_MOUSEBUTTON, QS_MOUSEMOVE, QS_PAINT, QS_POSTMESSAGE, QS_RAWINPUT, QS_SENDMESSAGE, QS_TIMER, _win32_GetQueueStatus, _win32_getqueuestatus_cpp, winmsg.getqueuestatus, winui._win32_getqueuestatus, winuser/GetQueueStatus
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
An input, <a href="https://msdn.microsoft.com/419e3f05-35ec-4e48-b24d-ab98df687b20">WM_TIMER</a>, <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a>, <a href="https://msdn.microsoft.com/28d87c2f-b2bb-4176-910b-0addea6beb93">WM_HOTKEY</a>, or posted message is in the queue.

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
A <a href="https://msdn.microsoft.com/28d87c2f-b2bb-4176-910b-0addea6beb93">WM_HOTKEY</a> message is in the queue.

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
A <a href="https://msdn.microsoft.com/67d9d82d-fab0-4aec-a337-7a9cb2b0b586">WM_KEYUP</a>, <a href="https://msdn.microsoft.com/0e37149f-445c-4b20-ad68-fdf39428ac91">WM_KEYDOWN</a>, <a href="https://msdn.microsoft.com/a4f62575-fb84-4390-a1d1-1a62629de55f">WM_SYSKEYUP</a>, or <a href="https://msdn.microsoft.com/a3c03dbf-1be7-49ff-b931-1981786b74ce">WM_SYSKEYDOWN</a> message is in the queue.

</td>
</tr>
<tr>
<td width="40%"><a id="QS_MOUSE"></a><a id="qs_mouse"></a><dl>
<dt><b>QS_MOUSE</b></dt>
<dt>(QS_MOUSEMOVE | QS_MOUSEBUTTON)</dt>
</dl>
</td>
<td width="60%">
A <a href="https://msdn.microsoft.com/9b99387e-e176-4b20-a05a-bc75928a1367">WM_MOUSEMOVE</a> message or mouse-button message (<a href="https://msdn.microsoft.com/6efa298f-85f7-40ab-a64b-16b5071f2437">WM_LBUTTONUP</a>, <a href="https://msdn.microsoft.com/da1a7d7c-6e49-4097-8b43-dcee7bd5fb3f">WM_RBUTTONDOWN</a>, and so on).

</td>
</tr>
<tr>
<td width="40%"><a id="QS_MOUSEBUTTON"></a><a id="qs_mousebutton"></a><dl>
<dt><b>QS_MOUSEBUTTON</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
A mouse-button message (<a href="https://msdn.microsoft.com/6efa298f-85f7-40ab-a64b-16b5071f2437">WM_LBUTTONUP</a>, <a href="https://msdn.microsoft.com/da1a7d7c-6e49-4097-8b43-dcee7bd5fb3f">WM_RBUTTONDOWN</a>, and so on).

</td>
</tr>
<tr>
<td width="40%"><a id="QS_MOUSEMOVE"></a><a id="qs_mousemove"></a><dl>
<dt><b>QS_MOUSEMOVE</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
A <a href="https://msdn.microsoft.com/9b99387e-e176-4b20-a05a-bc75928a1367">WM_MOUSEMOVE</a> message is in the queue.

</td>
</tr>
<tr>
<td width="40%"><a id="QS_PAINT"></a><a id="qs_paint"></a><dl>
<dt><b>QS_PAINT</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
A <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a> message is in the queue.

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
A raw input message is in the queue. For more information, see <a href="https://msdn.microsoft.com/a2afdb80-d68a-4c33-826f-96739d239cd9">Raw Input</a>.

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
A <a href="https://msdn.microsoft.com/419e3f05-35ec-4e48-b24d-ab98df687b20">WM_TIMER</a> message is in the queue.

</td>
</tr>
</table>
 


## -returns



Type: <strong>Type: <b>DWORD</b>
</strong>

The high-order word of the return value indicates the types of messages currently in the queue. The low-order word indicates the types of messages that have been added to the queue and that are still in the queue since the last call to the <b>GetQueueStatus</b>, <a href="https://msdn.microsoft.com/e92266a7-86ac-43f4-b0eb-762e145a1017">GetMessage</a>, or <a href="https://msdn.microsoft.com/b9f5baa4-8166-4d6e-b416-df023aed9bad">PeekMessage</a> function. 




## -remarks



The presence of a QS_ flag in the return value does not guarantee that a subsequent call to the <a href="https://msdn.microsoft.com/e92266a7-86ac-43f4-b0eb-762e145a1017">GetMessage</a> or <a href="https://msdn.microsoft.com/b9f5baa4-8166-4d6e-b416-df023aed9bad">PeekMessage</a> function will return a message. <b>GetMessage</b> and <b>PeekMessage</b> perform some internal filtering that may cause the message to be processed internally. For this reason, the return value from <b>GetQueueStatus</b> should be considered only a hint as to whether <b>GetMessage</b> or <b>PeekMessage</b> should be called. 

The <b>QS_ALLPOSTMESSAGE</b> and <b>QS_POSTMESSAGE</b> flags differ in when they are cleared. <b>QS_POSTMESSAGE</b> is cleared when you call <a href="https://msdn.microsoft.com/e92266a7-86ac-43f4-b0eb-762e145a1017">GetMessage</a> or <a href="https://msdn.microsoft.com/b9f5baa4-8166-4d6e-b416-df023aed9bad">PeekMessage</a>, whether or not you are filtering messages. <b>QS_ALLPOSTMESSAGE</b> is cleared when you call <b>GetMessage</b> or <b>PeekMessage</b> without filtering messages (<i>wMsgFilterMin</i> and <i>wMsgFilterMax</i> are 0). This can be useful when you call <b>PeekMessage</b> multiple times to get messages in different ranges. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/5d76901c-bb7e-4a84-b449-f0d58ebf31d8">GetInputState</a>



<a href="https://msdn.microsoft.com/e92266a7-86ac-43f4-b0eb-762e145a1017">GetMessage</a>



<a href="https://msdn.microsoft.com/885bb607-3ec0-4e24-9f55-fbdfb1c538a1">Messages and Message Queues</a>



<a href="https://msdn.microsoft.com/b9f5baa4-8166-4d6e-b416-df023aed9bad">PeekMessage</a>



<b>Reference</b>
 

 

