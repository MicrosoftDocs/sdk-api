---
UID: NF:winuser.DispatchMessage
title: DispatchMessage function (winuser.h)
description: Dispatches a message to a window procedure. It is typically used to dispatch a message retrieved by the GetMessage function.helpviewer_keywords: ["DispatchMessage","DispatchMessage function [Windows and Messages]","DispatchMessageA","DispatchMessageW","_win32_DispatchMessage","_win32_dispatchmessage_cpp","winmsg.dispatchmessage","winui._win32_dispatchmessage","winuser/DispatchMessage","winuser/DispatchMessageA","winuser/DispatchMessageW"]
old-location: winmsg\dispatchmessage.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\dispatchmessage.htm
ms.date: 12/05/2018
ms.keywords: DispatchMessage, DispatchMessage function [Windows and Messages], DispatchMessageA, DispatchMessageW, _win32_DispatchMessage, _win32_dispatchmessage_cpp, winmsg.dispatchmessage, winui._win32_dispatchmessage, winuser/DispatchMessage, winuser/DispatchMessageA, winuser/DispatchMessageW
f1_keywords:
- winuser/DispatchMessage
dev_langs:
- c++
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
- DispatchMessage
- DispatchMessageA
- DispatchMessageW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DispatchMessage function


## -description


Dispatches a message to a window procedure. It is typically used to dispatch a message retrieved by the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a> function.


## -parameters




### -param lpMsg [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-msg">MSG</a>*</b>

A pointer to a structure that contains the message.


## -returns



Type: <b>LRESULT</b>

The return value specifies the value returned by the window procedure. Although its meaning depends on the message being dispatched, the return value generally is ignored.




## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> structure must contain valid message values. If the <i>lpmsg</i> parameter points to a <a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-timer">WM_TIMER</a> message and the <i>lParam</i> parameter of the <b>WM_TIMER</b> message is not <b>NULL</b>, <i>lParam</i> points to a function that is called instead of the window procedure. 

Note that the application is responsible for retrieving and dispatching input messages to the dialog box. Most applications use the main message loop for this. However, to permit the user to move to and to select controls by using the keyboard, the application must call <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-isdialogmessagea">IsDialogMessage</a>. For more information, see <a href="https://docs.microsoft.com/windows/desktop/dlgbox/dlgbox-programming-considerations">Dialog Box Keyboard Interface</a>.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/winmsg/using-messages-and-message-queues">Creating a Message Loop</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-isdialogmessagea">IsDialogMessage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-msg">MSG</a>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/messages-and-message-queues">Messages and Message Queues</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-translatemessage">TranslateMessage</a>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-timer">WM_TIMER</a>
 

 

