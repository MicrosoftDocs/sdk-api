---
UID: NF:winuser.DispatchMessageW
title: DispatchMessageW function
author: windows-sdk-content
description: Dispatches a message to a window procedure. It is typically used to dispatch a message retrieved by the GetMessage function.
old-location: winmsg\dispatchmessage.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\dispatchmessage.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DispatchMessage, DispatchMessage function [Windows and Messages], DispatchMessageA, DispatchMessageW, _win32_DispatchMessage, _win32_dispatchmessage_cpp, winmsg.dispatchmessage, winui._win32_dispatchmessage, winuser/DispatchMessage, winuser/DispatchMessageA, winuser/DispatchMessageW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DispatchMessageW (Unicode) and DispatchMessageA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
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
 - DispatchMessage
 - DispatchMessageA
 - DispatchMessageW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# DispatchMessageW function


## -description


Dispatches a message to a window procedure. It is typically used to dispatch a message retrieved by the <a href="https://msdn.microsoft.com/e92266a7-86ac-43f4-b0eb-762e145a1017">GetMessage</a> function.


## -parameters




### -param lpMsg [in]

Type: <b>const <a href="https://msdn.microsoft.com/fee176ba-ad07-4145-ab4d-1b8c335fd100">MSG</a>*</b>

A pointer to a structure that contains the message.


## -returns



Type: <strong>Type: <b>LRESULT</b>
</strong>

The return value specifies the value returned by the window procedure. Although its meaning depends on the message being dispatched, the return value generally is ignored.




## -remarks



The <a href="https://msdn.microsoft.com/fee176ba-ad07-4145-ab4d-1b8c335fd100">MSG</a> structure must contain valid message values. If the <i>lpmsg</i> parameter points to a <a href="https://msdn.microsoft.com/419e3f05-35ec-4e48-b24d-ab98df687b20">WM_TIMER</a> message and the <i>lParam</i> parameter of the <b>WM_TIMER</b> message is not <b>NULL</b>, <i>lParam</i> points to a function that is called instead of the window procedure. 

Note that the application is responsible for retrieving and dispatching input messages to the dialog box. Most applications use the main message loop for this. However, to permit the user to move to and to select controls by using the keyboard, the application must call <a href="https://msdn.microsoft.com/0afa23a3-f552-40f9-9713-e7bf790ba25c">IsDialogMessage</a>. For more information, see <a href="https://msdn.microsoft.com/49024a0f-ea92-4d56-b063-8e5fcdbd884a">Dialog Box Keyboard Interface</a>.


#### Examples

For an example, see <a href="using_messages_and_message_queues.htm">Creating a Message Loop</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e92266a7-86ac-43f4-b0eb-762e145a1017">GetMessage</a>



<a href="https://msdn.microsoft.com/0afa23a3-f552-40f9-9713-e7bf790ba25c">IsDialogMessage</a>



<a href="https://msdn.microsoft.com/fee176ba-ad07-4145-ab4d-1b8c335fd100">MSG</a>



<a href="https://msdn.microsoft.com/885bb607-3ec0-4e24-9f55-fbdfb1c538a1">Messages and Message Queues</a>



<a href="https://msdn.microsoft.com/b9f5baa4-8166-4d6e-b416-df023aed9bad">PeekMessage</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/41c2baf4-6426-4789-919c-ab8ff9be8679">TranslateMessage</a>



<a href="https://msdn.microsoft.com/419e3f05-35ec-4e48-b24d-ab98df687b20">WM_TIMER</a>
 

 

