---
UID: NF:winuser.DispatchMessageW
title: DispatchMessageW function
author: windows-sdk-content
description: Dispatches a message to a window procedure. It is typically used to dispatch a message retrieved by the GetMessage function.
old-location: winmsg\dispatchmessage.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\dispatchmessage.htm
ms.author: windowssdkdev
ms.date: 03/29/2018
ms.keywords: DispatchMessage, DispatchMessage function [Windows and Messages], DispatchMessageA, DispatchMessageW, _win32_DispatchMessage, _win32_dispatchmessage_cpp, winmsg.dispatchmessage, winui._win32_dispatchmessage, winuser/DispatchMessage, winuser/DispatchMessageA, winuser/DispatchMessageW
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
req.unicode-ansi: DispatchMessageW (Unicode) and DispatchMessageA (ANSI)
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


Dispatches a message to a window procedure. It is typically used to dispatch a message retrieved by the <a href="https://msdn.microsoft.com/library/ms644936(v=VS.85).aspx">GetMessage</a> function.


## -parameters




### -param lpMsg

TBD




#### - lpmsg [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/ms644958(v=VS.85).aspx">MSG</a>*</b>

A pointer to a structure that contains the message.


## -returns



Type: <strong>Type: <b>LRESULT</b>
</strong>

The return value specifies the value returned by the window procedure. Although its meaning depends on the message being dispatched, the return value generally is ignored.




## -remarks



The <a href="https://msdn.microsoft.com/library/ms644958(v=VS.85).aspx">MSG</a> structure must contain valid message values. If the <i>lpmsg</i> parameter points to a <a href="https://msdn.microsoft.com/library/ms644902(v=VS.85).aspx">WM_TIMER</a> message and the <i>lParam</i> parameter of the <b>WM_TIMER</b> message is not <b>NULL</b>, <i>lParam</i> points to a function that is called instead of the window procedure. 


Note that the application is responsible for retrieving and dispatching input messages to the dialog box. Most applications use the main message loop for this. However, to permit the user to move to and to select controls by using the keyboard, the application must call <a href="https://msdn.microsoft.com/library/ms645498(v=VS.85).aspx">IsDialogMessage</a>. For more information, see <a href="https://msdn.microsoft.com/library/ms644995(v=VS.85).aspx">Dialog Box Keyboard Interface</a>.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/library/ms644928(v=VS.85).aspx">Creating a Message Loop</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/ms644936(v=VS.85).aspx">GetMessage</a>



<a href="https://msdn.microsoft.com/library/ms645498(v=VS.85).aspx">IsDialogMessage</a>



<a href="https://msdn.microsoft.com/library/ms644958(v=VS.85).aspx">MSG</a>



<a href="https://msdn.microsoft.com/library/ms632590(v=VS.85).aspx">Messages and Message Queues</a>



<a href="https://msdn.microsoft.com/library/ms644943(v=VS.85).aspx">PeekMessage</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/ms644955(v=VS.85).aspx">TranslateMessage</a>



<a href="https://msdn.microsoft.com/library/ms644902(v=VS.85).aspx">WM_TIMER</a>
 

 

