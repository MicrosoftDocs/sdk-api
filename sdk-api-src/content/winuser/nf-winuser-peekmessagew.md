---
UID: NF:winuser.PeekMessageW
title: PeekMessageW function
author: windows-sdk-content
description: Dispatches incoming sent messages, checks the thread message queue for a posted message, and retrieves the message (if any exist).
old-location: winmsg\peekmessage.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\peekmessage.htm
ms.author: windowssdkdev
ms.date: 03/29/2018
ms.keywords: PM_NOREMOVE, PM_NOYIELD, PM_QS_INPUT, PM_QS_PAINT, PM_QS_POSTMESSAGE, PM_QS_SENDMESSAGE, PM_REMOVE, PeekMessage, PeekMessage function [Windows and Messages], PeekMessageA, PeekMessageW, _win32_PeekMessage, _win32_peekmessage_cpp, winmsg.peekmessage, winui._win32_peekmessage, winuser/PeekMessage, winuser/PeekMessageA, winuser/PeekMessageW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: POINTER_DEVICE_TYPE
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
 - PeekMessage
 - PeekMessageA
 - PeekMessageW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# PeekMessageW function


## -description


Dispatches incoming sent messages, checks the thread message queue for a posted message, and retrieves the message (if any exist).


## -parameters




### -param lpMsg [out]

Type: <b>LPMSG</b>

A pointer to an <a href="https://msdn.microsoft.com/fee176ba-ad07-4145-ab4d-1b8c335fd100">MSG</a> structure that receives message information.


### -param hWnd [in, optional]

Type: <b>HWND</b>

A handle to the window whose messages are to be retrieved. The window must belong to the current thread. 



If <i>hWnd</i> is <b>NULL</b>, <b>PeekMessage</b> retrieves messages for any window that belongs to the current thread, and any messages on the current thread's message queue whose <b>hwnd</b> value is <b>NULL</b> (see the <a href="https://msdn.microsoft.com/fee176ba-ad07-4145-ab4d-1b8c335fd100">MSG</a> structure). Therefore if hWnd is <b>NULL</b>, both window messages and thread messages are processed.

 If <i>hWnd</i> is -1, <b>PeekMessage</b> retrieves only messages on the current thread's message queue whose <b>hwnd</b> value is <b>NULL</b>, that is, thread messages as posted by  <a href="https://msdn.microsoft.com/5357de37-1e44-4e4a-bdae-b5a386032dd4">PostMessage</a> (when the <i>hWnd</i> parameter is <b>NULL</b>) or <a href="https://msdn.microsoft.com/c418cb0e-1b9f-4ca8-8b02-e6901f7744a6">PostThreadMessage</a>.


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

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PM_NOREMOVE"></a><a id="pm_noremove"></a><dl>
<dt><b>PM_NOREMOVE</b></dt>
<dt>0x0000</dt>
</dl>
</td>
<td width="60%">
Messages are not removed from the queue after processing by <b>PeekMessage</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="PM_REMOVE"></a><a id="pm_remove"></a><dl>
<dt><b>PM_REMOVE</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Messages are removed from the queue after processing by <b>PeekMessage</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="PM_NOYIELD"></a><a id="pm_noyield"></a><dl>
<dt><b>PM_NOYIELD</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Prevents the system from releasing any thread that is waiting for the caller to go idle (see <a href="https://msdn.microsoft.com/2a684921-36f1-438c-895c-5bebc242635a">WaitForInputIdle</a>).

Combine this value with either <b>PM_NOREMOVE</b> or <b>PM_REMOVE</b>.

</td>
</tr>
</table>
 


By default, all message types are processed. To specify that only certain message should be processed, specify one or more of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PM_QS_INPUT"></a><a id="pm_qs_input"></a><dl>
<dt><b>PM_QS_INPUT</b></dt>
<dt>(QS_INPUT &lt;&lt; 16)</dt>
</dl>
</td>
<td width="60%">
 Process mouse and keyboard messages.

</td>
</tr>
<tr>
<td width="40%"><a id="PM_QS_PAINT"></a><a id="pm_qs_paint"></a><dl>
<dt><b>PM_QS_PAINT</b></dt>
<dt>(QS_PAINT &lt;&lt; 16)</dt>
</dl>
</td>
<td width="60%">
 Process paint messages.

</td>
</tr>
<tr>
<td width="40%"><a id="PM_QS_POSTMESSAGE"></a><a id="pm_qs_postmessage"></a><dl>
<dt><b>PM_QS_POSTMESSAGE</b></dt>
<dt>((QS_POSTMESSAGE | QS_HOTKEY | QS_TIMER) &lt;&lt; 16)</dt>
</dl>
</td>
<td width="60%">
 Process all posted messages, including timers and hotkeys.  

</td>
</tr>
<tr>
<td width="40%"><a id="PM_QS_SENDMESSAGE"></a><a id="pm_qs_sendmessage"></a><dl>
<dt><b>PM_QS_SENDMESSAGE</b></dt>
<dt>(QS_SENDMESSAGE &lt;&lt; 16)</dt>
</dl>
</td>
<td width="60%">
 Process all sent messages.

</td>
</tr>
</table>
 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If a message is available, the return value is nonzero.

If no messages are available, the return value is zero. 




## -remarks



<b>PeekMessage</b> retrieves messages associated with the window identified by the <i>hWnd</i> parameter or any of its children as specified by the <a href="https://msdn.microsoft.com/cf6faf3d-d705-438a-9f1f-c1aed2041ad6">IsChild</a> function, and within the range of message values given by the <i>wMsgFilterMin</i> and <i>wMsgFilterMax</i> parameters. Note that an application can only use the low word in the <i>wMsgFilterMin</i> and <i>wMsgFilterMax</i> parameters; the high word is reserved for the system.

Note that <b>PeekMessage</b> always retrieves <a href="https://msdn.microsoft.com/a9bff5dc-cab8-4e08-838e-d92c87c265d6">WM_QUIT</a> messages, no matter which values you specify for <i>wMsgFilterMin</i> and <i>wMsgFilterMax</i>.

During this call, the system delivers pending,  nonqueued messages, that is, messages sent to windows owned by the calling thread using the <a href="https://msdn.microsoft.com/library/windows/hardware/jj151552">SendMessage</a>, <a href="https://msdn.microsoft.com/6246e7ae-da06-4b86-b0d5-1743522b1bda">SendMessageCallback</a>, <a href="https://msdn.microsoft.com/c8096383-9fdf-42b3-af98-0bfe0d02c656">SendMessageTimeout</a>, or <a href="https://msdn.microsoft.com/08767153-34f5-4d31-9705-5a1862b9dd10">SendNotifyMessage</a> function. Then the first queued message that matches the specified filter is retrieved. The system may also process internal events. If no filter is specified, messages are processed in the following order:

<ul>
<li>Sent messages </li>
<li>Posted messages </li>
<li>Input (hardware) messages and system internal events </li>
<li>Sent messages (again) </li>
<li>
<a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a> messages </li>
<li>
<a href="https://msdn.microsoft.com/419e3f05-35ec-4e48-b24d-ab98df687b20">WM_TIMER</a> messages </li>
</ul>
To retrieve input messages before posted messages, use the <i>wMsgFilterMin</i> and <i>wMsgFilterMax</i> parameters. 

The <b>PeekMessage</b> function normally does not remove <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a> messages from the queue. <b>WM_PAINT</b> messages remain in the queue until they are processed. However, if a <b>WM_PAINT</b> message has a <b>NULL</b> update region, <b>PeekMessage</b> does remove it from the queue.

 If a top-level window stops responding to messages for more than several seconds, the system considers the window to be not responding and replaces it with a ghost window that has the same z-order, location, size, and visual attributes. This allows the user to move it, resize it, or even close the application. However, these are the only actions available because the application is actually not responding. When an application is being debugged, the system does not generate a ghost window. 

<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. The output is in the mode of the window that the message is targeting. The calling thread is not taken into consideration.


#### Examples

For an example, see <a href="using_messages_and_message_queues.htm">Examining a Message Queue</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e92266a7-86ac-43f4-b0eb-762e145a1017">GetMessage</a>



<a href="https://msdn.microsoft.com/cf6faf3d-d705-438a-9f1f-c1aed2041ad6">IsChild</a>



<a href="https://msdn.microsoft.com/fee176ba-ad07-4145-ab4d-1b8c335fd100">MSG</a>



<a href="https://msdn.microsoft.com/885bb607-3ec0-4e24-9f55-fbdfb1c538a1">Messages and Message Queues</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/2a684921-36f1-438c-895c-5bebc242635a">WaitForInputIdle</a>



<a href="https://msdn.microsoft.com/154fc22f-ef7a-42df-9f5d-26f0d2a2773c">WaitMessage</a>
 

 

