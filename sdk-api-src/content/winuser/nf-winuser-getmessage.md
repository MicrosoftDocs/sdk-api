---
UID: NF:winuser.GetMessage
title: GetMessage function
author: windows-sdk-content
description: Retrieves a message from the calling thread's message queue. The function dispatches incoming sent messages until a posted message is available for retrieval.
old-location: winmsg\getmessage.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\getmessage.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetMessage, GetMessage function [Windows and Messages], GetMessageA, GetMessageW, _win32_GetMessage, _win32_getmessage_cpp, winmsg.getmessage, winui._win32_getmessage, winuser/GetMessage, winuser/GetMessageA, winuser/GetMessageW
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
req.unicode-ansi: GetMessageW (Unicode) and GetMessageA (ANSI)
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
 - GetMessage
 - GetMessageA
 - GetMessageW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetMessage function


## -description


Retrieves a message from the calling thread's message queue. The function dispatches incoming sent messages until a posted message is available for retrieval. 
			

Unlike <b>GetMessage</b>, the <a href="https://msdn.microsoft.com/en-us/library/ms644943(v=VS.85).aspx">PeekMessage</a> function does not wait for a message to be posted before returning.


## -parameters




### -param lpMsg [out]

Type: <b>LPMSG</b>

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms644958(v=VS.85).aspx">MSG</a> structure that receives message information from the thread's message queue.


### -param hWnd [in, optional]

Type: <b>HWND</b>

A handle to the window whose messages are to be retrieved. The window must belong to the current thread. 


If <i>hWnd</i> is <b>NULL</b>, <b>GetMessage</b> retrieves messages for any window that belongs to the current thread, and any messages on the current thread's message queue whose <b>hwnd</b> value is <b>NULL</b> (see the <a href="https://msdn.microsoft.com/en-us/library/ms644958(v=VS.85).aspx">MSG</a> structure). Therefore if hWnd is <b>NULL</b>, both window messages and thread messages are processed.

 If <i>hWnd</i> is -1, <b>GetMessage</b> retrieves only messages on the current thread's message queue whose <b>hwnd</b> value is <b>NULL</b>,  that is, thread messages as posted by  <a href="https://msdn.microsoft.com/en-us/library/ms644944(v=VS.85).aspx">PostMessage</a> (when the <i>hWnd</i> parameter is <b>NULL</b>) or <a href="https://msdn.microsoft.com/en-us/library/ms644946(v=VS.85).aspx">PostThreadMessage</a>.


### -param wMsgFilterMin [in]

Type: <b>UINT</b>

The integer value of the lowest message value to be retrieved. Use <b>WM_KEYFIRST</b> (0x0100) to specify the first keyboard message or <b>WM_MOUSEFIRST</b> (0x0200) to specify the first mouse message. 

Use <a href="https://msdn.microsoft.com/en-us/library/ms645590(v=VS.85).aspx">WM_INPUT</a> here and in <i>wMsgFilterMax</i> to specify only the <b>WM_INPUT</b> messages.

If <i>wMsgFilterMin</i> and <i>wMsgFilterMax</i> are both zero, <b>GetMessage</b> returns all available messages (that is, no range filtering is performed). 


### -param wMsgFilterMax [in]

Type: <b>UINT</b>

The integer value of the highest message value to be retrieved. Use <b>WM_KEYLAST</b> to specify the last keyboard message or <b>WM_MOUSELAST</b> to specify the last mouse message. 
					

Use <a href="https://msdn.microsoft.com/en-us/library/ms645590(v=VS.85).aspx">WM_INPUT</a> here and in <i>wMsgFilterMin</i> to specify only the <b>WM_INPUT</b> messages.

If <i>wMsgFilterMin</i> and <i>wMsgFilterMax</i> are both zero, <b>GetMessage</b> returns all available messages (that is, no range filtering is performed). 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function retrieves a message other than <a href="https://msdn.microsoft.com/en-us/library/ms632641(v=VS.85).aspx">WM_QUIT</a>, the return value is nonzero.

If the function retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms632641(v=VS.85).aspx">WM_QUIT</a> message, the return value is zero. 

If there is an error, the return value is -1. For example, the function fails if <i>hWnd</i> is an invalid window handle or <i>lpMsg</i> is an invalid pointer. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

Because the return value can be nonzero, zero, or -1, avoid code like this:


```
while (GetMessage( lpMsg, hWnd, 0, 0)) ...
```


The possibility of a -1 return value in the case that hWnd is an invalid parameter (such as referring to a window that has already been destroyed) means that such code can lead to fatal application errors. Instead, use code like this:


```
BOOL bRet;

while( (bRet = GetMessage( &msg, hWnd, 0, 0 )) != 0)
{ 
    if (bRet == -1)
    {
        // handle the error and possibly exit
    }
    else
    {
        TranslateMessage(&msg); 
        DispatchMessage(&msg); 
    }
}
```





## -remarks



An application typically uses the return value to determine whether to end the main message loop and exit the program. 

The <b>GetMessage</b> function retrieves messages associated with the window identified by the <i>hWnd</i> parameter or any of its children, as specified by the <a href="https://msdn.microsoft.com/en-us/library/ms633524(v=VS.85).aspx">IsChild</a> function, and within the range of message values given by the <i>wMsgFilterMin</i> and <i>wMsgFilterMax</i> parameters. Note that an application can only use the low word in the <i>wMsgFilterMin</i> and <i>wMsgFilterMax</i> parameters; the high word is reserved for the system.

Note that <b>GetMessage</b> always retrieves <a href="https://msdn.microsoft.com/en-us/library/ms632641(v=VS.85).aspx">WM_QUIT</a> messages, no matter which values you specify for <i>wMsgFilterMin</i> and <i>wMsgFilterMax</i>.

During this call, the system delivers pending, nonqueued messages, that is, messages sent to windows owned by the calling thread using the <a href="https://msdn.microsoft.com/en-us/library/ms644950(v=VS.85).aspx">SendMessage</a>, <a href="https://msdn.microsoft.com/en-us/library/ms644951(v=VS.85).aspx">SendMessageCallback</a>, <a href="https://msdn.microsoft.com/en-us/library/ms644952(v=VS.85).aspx">SendMessageTimeout</a>, or <a href="https://msdn.microsoft.com/en-us/library/ms644953(v=VS.85).aspx">SendNotifyMessage</a> function. Then the first queued message that matches the specified filter is retrieved. The system may also process internal events. If no filter is specified, messages are processed in the following order: 
				

<ul>
<li>Sent messages </li>
<li>Posted messages </li>
<li>Input (hardware) messages and system internal events </li>
<li>Sent messages (again) </li>
<li>
<a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a> messages </li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms644902(v=VS.85).aspx">WM_TIMER</a> messages </li>
</ul>
To retrieve input messages before posted messages, use the <i>wMsgFilterMin</i> and <i>wMsgFilterMax</i> parameters. 

<b>GetMessage</b> does not remove <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a> messages from the queue. The messages remain in the queue until processed. 

If a top-level window stops responding to messages for more than several seconds, the system considers the window to be not responding and replaces it with a ghost window that has the same z-order, location, size, and visual attributes. This allows the user to move it, resize it, or even close the application. However, these are the only actions available because the application is actually not responding. When in the debugger mode, the system does not generate a ghost window.

<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. The output is in the mode of the window that the message is targeting. The calling thread is not taken into consideration.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms644928(v=VS.85).aspx">Creating a Message Loop</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633524(v=VS.85).aspx">IsChild</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644958(v=VS.85).aspx">MSG</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632590(v=VS.85).aspx">Messages and Message Queues</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644943(v=VS.85).aspx">PeekMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644944(v=VS.85).aspx">PostMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644946(v=VS.85).aspx">PostThreadMessage</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644956(v=VS.85).aspx">WaitMessage</a>
 

 

