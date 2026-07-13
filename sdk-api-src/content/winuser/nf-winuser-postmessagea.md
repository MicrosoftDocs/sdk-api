---
UID: NF:winuser.PostMessageA
title: PostMessageA function (winuser.h)
description: Places (posts) a message in the message queue associated with the thread that created the specified window and returns without waiting for the thread to process the message. (ANSI)
helpviewer_keywords: ["HWND_BROADCAST", "PostMessageA", "winuser/PostMessageA"]
old-location: winmsg\postmessage.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\postmessage.htm
ms.date: 12/05/2018
ms.keywords: HWND_BROADCAST, PostMessage, PostMessage function [Windows and Messages], PostMessageA, PostMessageW, _win32_PostMessage, _win32_postmessage_cpp, winmsg.postmessage, winui._win32_postmessage, winuser/PostMessage, winuser/PostMessageA, winuser/PostMessageW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PostMessageA
 - winuser/PostMessageA
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
 - PostMessage
 - PostMessageA
 - PostMessageW
req.apiset: ext-ms-win-ntuser-message-l1-1-0 (introduced in Windows 8)
---

# PostMessageA function


## -description

Places (posts) a message in the message queue associated with the thread that created the specified window and returns without waiting for the thread to process the message.

To post a message in the message queue associated with a thread, use the <a href="/windows/desktop/api/winuser/nf-winuser-postthreadmessagea">PostThreadMessage</a> function.

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
The function behaves like a call to <a href="/windows/desktop/api/winuser/nf-winuser-postthreadmessagea">PostThreadMessage</a> with the <i>dwThreadId</i> parameter set to the identifier of the current thread.

</td>
</tr>
</table>
 

Starting with Windows Vista, message posting is subject to UIPI. The thread of a process can post messages only to message queues of threads in processes of lesser or equal integrity level.

### -param Msg [in]

Type: <b>UINT</b>

The message to be posted.

For lists of the system-provided messages, see <a href="/windows/desktop/winmsg/about-messages-and-message-queues">System-Defined Messages</a>.

### -param wParam [in]

Type: <b>WPARAM</b>

Additional message-specific information.

### -param lParam [in]

Type: <b>LPARAM</b>

Additional message-specific information.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

 When a message is blocked by UIPI the last error, retrieved with <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, is set to 5 (access denied).

Messages in a message queue are retrieved by calls to the <a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a> or <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> function.

Applications that need to communicate using <b>HWND_BROADCAST</b> should use the <a href="/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea">RegisterWindowMessage</a> function to obtain a unique message for inter-application communication.

The system only does marshalling for system messages (those in the range 0 to (<a href="/windows/desktop/winmsg/wm-user">WM_USER</a>-1)). To send other messages (those &gt;= <b>WM_USER</b>) to another process, you must do custom marshalling.

If you send a message in the range below <a href="/windows/desktop/winmsg/wm-user">WM_USER</a> to the asynchronous message functions (<b>PostMessage</b>, <a href="/windows/desktop/api/winuser/nf-winuser-sendnotifymessagea">SendNotifyMessage</a>, and <a href="/windows/desktop/api/winuser/nf-winuser-sendmessagecallbacka">SendMessageCallback</a>), its message parameters cannot include pointers. Otherwise, the operation will fail. The functions will return before the receiving thread has had a chance to process the message and the sender will free the memory before it is used.

Do not post the <a href="/windows/desktop/winmsg/wm-quit">WM_QUIT</a> message using <b>PostMessage</b>; use the <a href="/windows/desktop/api/winuser/nf-winuser-postquitmessage">PostQuitMessage</a> function.

 An accessibility application can use <b>PostMessage</b> to post <a href="/windows/desktop/inputdev/wm-appcommand">WM_APPCOMMAND</a> messages  to the shell to launch applications. This  functionality is not guaranteed to work for other types of applications.

A message queue can contain at most 10,000 messages. This limit should be sufficiently large.  If your application exceeds the limit, it should be redesigned to avoid consuming so many system resources. To adjust this limit, modify the following registry key.
				
<pre><b>HKEY_LOCAL_MACHINE</b>
   <b>SOFTWARE</b>
      <b>Microsoft</b>
         <b>Windows NT</b>
            <b>CurrentVersion</b>
               <b>Windows</b>
                  <b>USERPostMessageLimit</b></pre>

If the function fails, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to get extended error information. <b>GetLastError</b> returns <b>ERROR_NOT_ENOUGH_QUOTA</b> when the limit is hit.

The minimum acceptable value is 4000.

			


#### Examples

The following example shows how to post a private window message using the <b>PostMessage</b> function. Assume you defined a private window message called <b>WM_COMPLETE</b>: 


```cpp
#define        WM_COMPLETE     (WM_USER + 0)

```


You can post a message to the message queue associated with the thread that created the specified window as shown below:


```cpp
 WaitForSingleObject (pparams->hEvent, INFINITE) ;
 lTime = GetCurrentTime () ;
 PostMessage (pparams->hwnd, WM_COMPLETE, 0, lTime);

```


For more examples, see <a href="/windows/desktop/dataxchg/using-dynamic-data-exchange">Initiating a Data Link</a>.

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines PostMessage as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>



<a href="/windows/desktop/winmsg/messages-and-message-queues">Messages and Message Queues</a>



<a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>



<a href="/windows/desktop/api/winuser/nf-winuser-postquitmessage">PostQuitMessage</a>



<a href="/windows/desktop/api/winuser/nf-winuser-postthreadmessagea">PostThreadMessage</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea">RegisterWindowMessage</a>



<a href="/windows/desktop/api/winuser/nf-winuser-sendmessagecallbacka">SendMessageCallback</a>



<a href="/windows/desktop/api/winuser/nf-winuser-sendnotifymessagea">SendNotifyMessage</a>
