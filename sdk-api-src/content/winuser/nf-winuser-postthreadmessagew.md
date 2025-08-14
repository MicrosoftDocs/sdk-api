---
UID: NF:winuser.PostThreadMessageW
title: PostThreadMessageW function (winuser.h)
description: Posts a message to the message queue of the specified thread. It returns without waiting for the thread to process the message. (Unicode)
helpviewer_keywords: ["PostThreadMessage", "PostThreadMessage function [Windows and Messages]", "PostThreadMessageW", "_win32_PostThreadMessage", "_win32_postthreadmessage_cpp", "winmsg.postthreadmessage", "winui._win32_postthreadmessage", "winuser/PostThreadMessage", "winuser/PostThreadMessageW"]
old-location: winmsg\postthreadmessage.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\postthreadmessage.htm
ms.date: 12/05/2018
ms.keywords: PostThreadMessage, PostThreadMessage function [Windows and Messages], PostThreadMessageA, PostThreadMessageW, _win32_PostThreadMessage, _win32_postthreadmessage_cpp, winmsg.postthreadmessage, winui._win32_postthreadmessage, winuser/PostThreadMessage, winuser/PostThreadMessageA, winuser/PostThreadMessageW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PostThreadMessageW (Unicode) and PostThreadMessageA (ANSI)
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
 - PostThreadMessageW
 - winuser/PostThreadMessageW
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
 - PostThreadMessage
 - PostThreadMessageA
 - PostThreadMessageW
req.apiset: ext-ms-win-ntuser-message-l1-1-0 (introduced in Windows 8)
---

# PostThreadMessageW function


## -description

Posts a message to the message queue of the specified thread. It returns without waiting for the thread to process the message.

## -parameters

### -param idThread [in]

Type: <b>DWORD</b>

The identifier of the thread to which the message is to be posted.

The function fails if the specified thread does not have a message queue. The system creates a thread's message queue when the thread makes its first call to one of the User or GDI functions. For more information, see the Remarks section.

Message posting is subject to UIPI. The thread of a process can post messages only to posted-message queues of threads in processes of lesser or equal integrity level.

 This thread must have the <b>SE_TCB_NAME</b> privilege to post a message to a thread that belongs to a process with the same locally unique identifier (LUID) but is in a different desktop. Otherwise, the function fails and returns <b>ERROR_INVALID_THREAD_ID</b>.

 This thread must either belong to the same desktop as the calling thread or to a process with the same LUID. Otherwise, the function fails and returns <b>ERROR_INVALID_THREAD_ID</b>.

### -param Msg [in]

Type: <b>UINT</b>

The type of message to be posted.

### -param wParam [in]

Type: <b>WPARAM</b>

Additional message-specific information.

### -param lParam [in]

Type: <b>LPARAM</b>

Additional message-specific information.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. <b>GetLastError</b> returns <b>ERROR_INVALID_THREAD_ID</b> if <i>idThread</i> is not a valid thread identifier, or if the thread specified by <i>idThread</i> does not have a message queue. <b>GetLastError</b> returns <b>ERROR_NOT_ENOUGH_QUOTA</b> when the message limit is hit.

## -remarks

 When a message is blocked by UIPI the last error, retrieved with <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, is set to 5 (access denied).

The thread to which the message is posted must have created a message queue, or else the call to <b>PostThreadMessage</b> fails. Use the following method to handle this situation. 

				

<ul>
<li>
Create an event object, then create the thread.

</li>
<li>
Use the <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a> function to wait for the event to be set to the signaled state before calling <b>PostThreadMessage</b>.

</li>
<li>
In the thread to which the message will be posted, call <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> as shown here to force the system to create the message queue.

<code>PeekMessage(&amp;msg, NULL, WM_USER, WM_USER, PM_NOREMOVE)</code>

</li>
<li>
Set the event, to indicate that the thread is ready to receive posted messages.

</li>
</ul>
The thread to which the message is posted retrieves the message by calling the <a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a> or <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> function. The <b>hwnd</b> member of the returned <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> structure is <b>NULL</b>.

Messages posted by <b>PostThreadMessage</b> are not associated with a window. As a general rule, messages that are not associated with a window cannot be dispatched by the <a href="/windows/desktop/api/winuser/nf-winuser-dispatchmessage">DispatchMessage</a> function. Therefore, if the recipient thread is in a modal loop (as used by <a href="/windows/desktop/api/winuser/nf-winuser-messagebox">MessageBox</a> or <a href="/windows/desktop/api/winuser/nf-winuser-dialogboxa">DialogBox</a>), the messages will be lost. To intercept thread messages while in a modal loop, use a thread-specific hook.

The system only does marshalling for system messages (those in the range 0 to (<a href="/windows/desktop/winmsg/wm-user">WM_USER</a>-1)). To send other messages (those &gt;= <b>WM_USER</b>) to another process, you must do custom marshalling.

 There is a limit of 10,000 posted messages per message queue. This limit should be sufficiently large. If your application exceeds the limit, it should be redesigned to avoid consuming so many system resources. To adjust this limit, modify the following registry key.


<pre xml:space="preserve"><b>HKEY_LOCAL_MACHINE</b>
   <b>SOFTWARE</b>
      <b>Microsoft</b>
         <b>Windows NT</b>
            <b>CurrentVersion</b>
               <b>Windows</b>
                  <b>USERPostMessageLimit</b></pre>


The minimum acceptable value is 4000.
			





> [!NOTE]
> The winuser.h header defines PostThreadMessage as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid">GetCurrentThreadId</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getwindowthreadprocessid">GetWindowThreadProcessId</a>



<a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a>



<a href="/windows/desktop/winmsg/messages-and-message-queues">Messages and Message Queues</a>



<b>Other Resources</b>



<a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>



<a href="/windows/desktop/api/winuser/nf-winuser-postmessagea">PostMessage</a>



<b>Reference</b>



<a href="/windows/desktop/api/synchapi/nf-synchapi-sleep">Sleep</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a>
