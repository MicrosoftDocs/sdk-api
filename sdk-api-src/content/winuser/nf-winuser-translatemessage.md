---
UID: NF:winuser.TranslateMessage
title: TranslateMessage function
author: windows-sdk-content
description: Translates virtual-key messages into character messages. The character messages are posted to the calling thread's message queue, to be read the next time the thread calls the GetMessage or PeekMessage function.
old-location: winmsg\translatemessage.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\translatemessage.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TranslateMessage, TranslateMessage function [Windows and Messages], _win32_TranslateMessage, _win32_translatemessage_cpp, winmsg.translatemessage, winui._win32_translatemessage, winuser/TranslateMessage
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
req.unicode-ansi: 
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
 - TranslateMessage
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# TranslateMessage function


## -description


Translates virtual-key messages into character messages. The character messages are posted to the calling thread's message queue, to be read the next time the thread calls the <a href="https://msdn.microsoft.com/en-us/library/ms644936(v=VS.85).aspx">GetMessage</a> or <a href="https://msdn.microsoft.com/en-us/library/ms644943(v=VS.85).aspx">PeekMessage</a> function.


## -parameters




### -param lpMsg [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms644958(v=VS.85).aspx">MSG</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms644958(v=VS.85).aspx">MSG</a> structure that contains message information retrieved from the calling thread's message queue by using the <a href="https://msdn.microsoft.com/en-us/library/ms644936(v=VS.85).aspx">GetMessage</a> or <a href="https://msdn.microsoft.com/en-us/library/ms644943(v=VS.85).aspx">PeekMessage</a> function.


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the message is translated (that is, a character message is posted to the thread's message queue), the return value is nonzero.

If the message is <a href="https://msdn.microsoft.com/en-us/library/ms646280(v=VS.85).aspx">WM_KEYDOWN</a>, <a href="https://msdn.microsoft.com/en-us/library/ms646281(v=VS.85).aspx">WM_KEYUP</a>, <a href="https://msdn.microsoft.com/en-us/library/ms646286(v=VS.85).aspx">WM_SYSKEYDOWN</a>, or <a href="https://msdn.microsoft.com/en-us/library/ms646287(v=VS.85).aspx">WM_SYSKEYUP</a>, the return value is nonzero, regardless of the translation. 

If the message is not translated (that is, a character message is not posted to the thread's message queue), the return value is zero.




## -remarks



The <b>TranslateMessage</b> function does not modify the message pointed to by the <i>lpMsg</i> parameter. 


<a href="https://msdn.microsoft.com/en-us/library/ms646280(v=VS.85).aspx">WM_KEYDOWN</a> and <a href="https://msdn.microsoft.com/en-us/library/ms646281(v=VS.85).aspx">WM_KEYUP</a> combinations produce a <a href="https://msdn.microsoft.com/en-us/library/ms646276(v=VS.85).aspx">WM_CHAR</a> or <a href="https://msdn.microsoft.com/en-us/library/ms646277(v=VS.85).aspx">WM_DEADCHAR</a> message. <a href="https://msdn.microsoft.com/en-us/library/ms646286(v=VS.85).aspx">WM_SYSKEYDOWN</a> and <a href="https://msdn.microsoft.com/en-us/library/ms646287(v=VS.85).aspx">WM_SYSKEYUP</a> combinations produce a <a href="https://msdn.microsoft.com/en-us/library/ms646357(v=VS.85).aspx">WM_SYSCHAR</a> or <a href="https://msdn.microsoft.com/en-us/library/ms646285(v=VS.85).aspx">WM_SYSDEADCHAR</a> message. 

<b>TranslateMessage</b> produces <a href="https://msdn.microsoft.com/en-us/library/ms646276(v=VS.85).aspx">WM_CHAR</a> messages only for keys that are mapped to ASCII characters by the keyboard driver. 

If applications process virtual-key messages for some other purpose, they should not call <b>TranslateMessage</b>. For instance, an application should not call <b>TranslateMessage</b> if the <a href="https://msdn.microsoft.com/en-us/library/ms646373(v=VS.85).aspx">TranslateAccelerator</a> function returns a nonzero value. Note that the application is responsible for retrieving and dispatching input messages to the dialog box. Most applications use the main message loop for this. However, to permit the user to move to and to select controls by using the keyboard, the application must call <a href="https://msdn.microsoft.com/en-us/library/ms645498(v=VS.85).aspx">IsDialogMessage</a>. For more information, see  <a href="https://msdn.microsoft.com/en-us/library/ms644995(v=VS.85).aspx">Dialog Box Keyboard Interface</a>.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms644928(v=VS.85).aspx">Creating a Message Loop</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644936(v=VS.85).aspx">GetMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645498(v=VS.85).aspx">IsDialogMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632590(v=VS.85).aspx">Messages and Message Queues</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644943(v=VS.85).aspx">PeekMessage</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646373(v=VS.85).aspx">TranslateAccelerator</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646276(v=VS.85).aspx">WM_CHAR</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646277(v=VS.85).aspx">WM_DEADCHAR</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646280(v=VS.85).aspx">WM_KEYDOWN</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646281(v=VS.85).aspx">WM_KEYUP</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646357(v=VS.85).aspx">WM_SYSCHAR</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646285(v=VS.85).aspx">WM_SYSDEADCHAR</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646286(v=VS.85).aspx">WM_SYSKEYDOWN</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646287(v=VS.85).aspx">WM_SYSKEYUP</a>
 

 

