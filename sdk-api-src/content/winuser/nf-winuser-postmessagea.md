---
UID: NF:winuser.PostMessageA
title: PostMessageA function
author: windows-sdk-content
description: Places (posts) a message in the message queue associated with the thread that created the specified window and returns without waiting for the thread to process the message.
old-location: winmsg\postmessage.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\postmessage.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: HWND_BROADCAST, PostMessage, PostMessage function [Windows and Messages], PostMessageA, PostMessageW, _win32_PostMessage, _win32_postmessage_cpp, winmsg.postmessage, winui._win32_postmessage, winuser/PostMessage, winuser/PostMessageA, winuser/PostMessageW
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
req.unicode-ansi: PostMessageW (Unicode) and PostMessageA (ANSI)
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
 - PostMessage
 - PostMessageA
 - PostMessageW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- PostMessageA
: 
---

# PostMessageA function


## -description


Places (posts) a message in the message queue associated with the thread that created the specified window and returns without waiting for the thread to process the message.

To post a message in the message queue associated with a thread, use the <a href="https://msdn.microsoft.com/c418cb0e-1b9f-4ca8-8b02-e6901f7744a6">PostThreadMessage</a> function.


## -parameters




### -param hWnd [in, optional]

Type: <b>HWND</b>

A handle to the window whose window procedure is to receive the message. The following values have special meanings.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HWND_BROADCAST"></a><a id="hwnd_broadcast"></a><dl>
<dt><b>HWND_BROADCAST</b></dt>
<dt>((HWND)0xffff)</dt>
</dl>
</td>
<td width="60%">
The message is posted to all top-level windows in the system, including disabled or invisible unowned windows, overlapped windows, and pop-up windows. The message is not posted to child windows.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>NULL</dt>
</dl>
</td>
<td width="60%">
The function behaves like a call to <a href="https://msdn.microsoft.com/c418cb0e-1b9f-4ca8-8b02-e6901f7744a6">PostThreadMessage</a> with the <i>dwThreadId</i> parameter set to the identifier of the current thread.

</td>
</tr>
</table>
 

Starting with Windows Vista, message posting is subject to UIPI. The thread of a process can post messages only to message queues of threads in processes of lesser or equal integrity level.


### -param Msg [in]

Type: <b>UINT</b>

The message to be posted.

For lists of the system-provided messages, see <a href="about_messages_and_message_queues.htm">System-Defined Messages</a>.


### -param wParam [in]

Type: <b>WPARAM</b>

Additional message-specific information.


### -param lParam [in]

Type: <b>LPARAM</b>

Additional message-specific information.


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. <b>GetLastError</b> returns <b>ERROR_NOT_ENOUGH_QUOTA</b> when the limit is hit. 




## -remarks



 When a message is blocked by UIPI the last error, retrieved with <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, is set to 5 (access denied).

Messages in a message queue are retrieved by calls to the <a href="https://msdn.microsoft.com/e92266a7-86ac-43f4-b0eb-762e145a1017">GetMessage</a> or <a href="https://msdn.microsoft.com/b9f5baa4-8166-4d6e-b416-df023aed9bad">PeekMessage</a> function.

Applications that need to communicate using <b>HWND_BROADCAST</b> should use the <a href="https://msdn.microsoft.com/51ddc767-ffce-42bf-885a-24b9ee1b25f0">RegisterWindowMessage</a> function to obtain a unique message for inter-application communication.

The system only does marshalling for system messages (those in the range 0 to (<a href="https://msdn.microsoft.com/4115c587-fcb4-4170-9948-fe33bcb8742a">WM_USER</a>-1)). To send other messages (those &gt;= <b>WM_USER</b>) to another process, you must do custom marshalling.

If you send a message in the range below <a href="https://msdn.microsoft.com/4115c587-fcb4-4170-9948-fe33bcb8742a">WM_USER</a> to the asynchronous message functions (<b>PostMessage</b>, <a href="https://msdn.microsoft.com/08767153-34f5-4d31-9705-5a1862b9dd10">SendNotifyMessage</a>, and <a href="https://msdn.microsoft.com/6246e7ae-da06-4b86-b0d5-1743522b1bda">SendMessageCallback</a>), its message parameters cannot include pointers. Otherwise, the operation will fail. The functions will return before the receiving thread has had a chance to process the message and the sender will free the memory before it is used.

Do not post the <a href="https://msdn.microsoft.com/a9bff5dc-cab8-4e08-838e-d92c87c265d6">WM_QUIT</a> message using <b>PostMessage</b>; use the <a href="https://msdn.microsoft.com/8abc09a0-d53a-44ff-a91b-ee602260763c">PostQuitMessage</a> function.

 An accessibility application can use <b>PostMessage</b> to post <a href="https://msdn.microsoft.com/ffcdfc44-dbfa-42d4-8749-b33bf0e4de0c">WM_APPCOMMAND</a> messages  to the shell to launch applications. This  functionality is not guaranteed to work for other types of applications.

There is a limit of 10,000 posted messages per message queue. This limit should be sufficiently large.  If your application exceeds the limit, it should be redesigned to avoid consuming so many system resources. To adjust this limit, modify the following registry key.
				
				


<pre xml:space="preserve"><b>HKEY_LOCAL_MACHINE</b>
   <b>SOFTWARE</b>
      <b>Microsoft</b>
         <b>Windows NT</b>
            <b>CurrentVersion</b>
               <b>Windows</b>
                  <b>USERPostMessageLimit</b></pre>


The minimum acceptable value is 4000.

			


#### Examples

The following example shows how to post a private window message using the <b>PostMessage</b> function. Assume you defined a private window message called <b>WM_COMPLETE</b>: 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#define        WM_COMPLETE     (WM_USER + 0)
</pre>
</td>
</tr>
</table></span></div>
You can post a message to the message queue associated with the thread that created the specified window as shown below:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre> WaitForSingleObject (pparams-&gt;hEvent, INFINITE) ;
 lTime = GetCurrentTime () ;
 PostMessage (pparams-&gt;hwnd, WM_COMPLETE, 0, lTime);
</pre>
</td>
</tr>
</table></span></div>
For more examples, see <a href="https://msdn.microsoft.com/6d94403b-64b4-4763-868a-3b94431dab79">Initiating a Data Link</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e92266a7-86ac-43f4-b0eb-762e145a1017">GetMessage</a>



<a href="https://msdn.microsoft.com/885bb607-3ec0-4e24-9f55-fbdfb1c538a1">Messages and Message Queues</a>



<a href="https://msdn.microsoft.com/b9f5baa4-8166-4d6e-b416-df023aed9bad">PeekMessage</a>



<a href="https://msdn.microsoft.com/8abc09a0-d53a-44ff-a91b-ee602260763c">PostQuitMessage</a>



<a href="https://msdn.microsoft.com/c418cb0e-1b9f-4ca8-8b02-e6901f7744a6">PostThreadMessage</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/51ddc767-ffce-42bf-885a-24b9ee1b25f0">RegisterWindowMessage</a>



<a href="https://msdn.microsoft.com/6246e7ae-da06-4b86-b0d5-1743522b1bda">SendMessageCallback</a>



<a href="https://msdn.microsoft.com/08767153-34f5-4d31-9705-5a1862b9dd10">SendNotifyMessage</a>
 

 

