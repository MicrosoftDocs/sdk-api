---
UID: NF:winuser.TranslateMessage
title: TranslateMessage function
author: windows-sdk-content
description: Translates virtual-key messages into character messages. The character messages are posted to the calling thread's message queue, to be read the next time the thread calls the GetMessage or PeekMessage function.
old-location: winmsg\translatemessage.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\translatemessage.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: TranslateMessage, TranslateMessage function [Windows and Messages], _win32_TranslateMessage, _win32_translatemessage_cpp, winmsg.translatemessage, winui._win32_translatemessage, winuser/TranslateMessage
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
 - TranslateMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TranslateMessage function


## -description


Translates virtual-key messages into character messages. The character messages are posted to the calling thread's message queue, to be read the next time the thread calls the <a href="https://msdn.microsoft.com/e92266a7-86ac-43f4-b0eb-762e145a1017">GetMessage</a> or <a href="https://msdn.microsoft.com/b9f5baa4-8166-4d6e-b416-df023aed9bad">PeekMessage</a> function.


## -parameters




### -param lpMsg [in]

Type: <b>const <a href="https://msdn.microsoft.com/fee176ba-ad07-4145-ab4d-1b8c335fd100">MSG</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/fee176ba-ad07-4145-ab4d-1b8c335fd100">MSG</a> structure that contains message information retrieved from the calling thread's message queue by using the <a href="https://msdn.microsoft.com/e92266a7-86ac-43f4-b0eb-762e145a1017">GetMessage</a> or <a href="https://msdn.microsoft.com/b9f5baa4-8166-4d6e-b416-df023aed9bad">PeekMessage</a> function.


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the message is translated (that is, a character message is posted to the thread's message queue), the return value is nonzero.

If the message is <a href="https://msdn.microsoft.com/0e37149f-445c-4b20-ad68-fdf39428ac91">WM_KEYDOWN</a>, <a href="https://msdn.microsoft.com/67d9d82d-fab0-4aec-a337-7a9cb2b0b586">WM_KEYUP</a>, <a href="https://msdn.microsoft.com/a3c03dbf-1be7-49ff-b931-1981786b74ce">WM_SYSKEYDOWN</a>, or <a href="https://msdn.microsoft.com/a4f62575-fb84-4390-a1d1-1a62629de55f">WM_SYSKEYUP</a>, the return value is nonzero, regardless of the translation. 

If the message is not translated (that is, a character message is not posted to the thread's message queue), the return value is zero.




## -remarks



The <b>TranslateMessage</b> function does not modify the message pointed to by the <i>lpMsg</i> parameter. 


<a href="https://msdn.microsoft.com/0e37149f-445c-4b20-ad68-fdf39428ac91">WM_KEYDOWN</a> and <a href="https://msdn.microsoft.com/67d9d82d-fab0-4aec-a337-7a9cb2b0b586">WM_KEYUP</a> combinations produce a <a href="https://msdn.microsoft.com/7e45dc6f-ff68-4534-9e52-46e5f4110532">WM_CHAR</a> or <a href="https://msdn.microsoft.com/ada9a61c-dabf-447b-ae13-91803c097f0d">WM_DEADCHAR</a> message. <a href="https://msdn.microsoft.com/a3c03dbf-1be7-49ff-b931-1981786b74ce">WM_SYSKEYDOWN</a> and <a href="https://msdn.microsoft.com/a4f62575-fb84-4390-a1d1-1a62629de55f">WM_SYSKEYUP</a> combinations produce a <a href="https://msdn.microsoft.com/55987105-3c53-42e5-8fab-a3c9f2ca7273">WM_SYSCHAR</a> or <a href="https://msdn.microsoft.com/cf9a1171-a47c-4d7b-b351-31f41a893b20">WM_SYSDEADCHAR</a> message. 

<b>TranslateMessage</b> produces <a href="https://msdn.microsoft.com/7e45dc6f-ff68-4534-9e52-46e5f4110532">WM_CHAR</a> messages only for keys that are mapped to ASCII characters by the keyboard driver. 

If applications process virtual-key messages for some other purpose, they should not call <b>TranslateMessage</b>. For instance, an application should not call <b>TranslateMessage</b> if the <a href="https://msdn.microsoft.com/0d8a970c-68b2-45e6-8702-2490029c1e1d">TranslateAccelerator</a> function returns a nonzero value. Note that the application is responsible for retrieving and dispatching input messages to the dialog box. Most applications use the main message loop for this. However, to permit the user to move to and to select controls by using the keyboard, the application must call <a href="https://msdn.microsoft.com/0afa23a3-f552-40f9-9713-e7bf790ba25c">IsDialogMessage</a>. For more information, see  <a href="https://msdn.microsoft.com/49024a0f-ea92-4d56-b063-8e5fcdbd884a">Dialog Box Keyboard Interface</a>.


#### Examples

For an example, see <a href="using_messages_and_message_queues.htm">Creating a Message Loop</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e92266a7-86ac-43f4-b0eb-762e145a1017">GetMessage</a>



<a href="https://msdn.microsoft.com/0afa23a3-f552-40f9-9713-e7bf790ba25c">IsDialogMessage</a>



<a href="https://msdn.microsoft.com/885bb607-3ec0-4e24-9f55-fbdfb1c538a1">Messages and Message Queues</a>



<a href="https://msdn.microsoft.com/b9f5baa4-8166-4d6e-b416-df023aed9bad">PeekMessage</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/0d8a970c-68b2-45e6-8702-2490029c1e1d">TranslateAccelerator</a>



<a href="https://msdn.microsoft.com/7e45dc6f-ff68-4534-9e52-46e5f4110532">WM_CHAR</a>



<a href="https://msdn.microsoft.com/ada9a61c-dabf-447b-ae13-91803c097f0d">WM_DEADCHAR</a>



<a href="https://msdn.microsoft.com/0e37149f-445c-4b20-ad68-fdf39428ac91">WM_KEYDOWN</a>



<a href="https://msdn.microsoft.com/67d9d82d-fab0-4aec-a337-7a9cb2b0b586">WM_KEYUP</a>



<a href="https://msdn.microsoft.com/55987105-3c53-42e5-8fab-a3c9f2ca7273">WM_SYSCHAR</a>



<a href="https://msdn.microsoft.com/cf9a1171-a47c-4d7b-b351-31f41a893b20">WM_SYSDEADCHAR</a>



<a href="https://msdn.microsoft.com/a3c03dbf-1be7-49ff-b931-1981786b74ce">WM_SYSKEYDOWN</a>



<a href="https://msdn.microsoft.com/a4f62575-fb84-4390-a1d1-1a62629de55f">WM_SYSKEYUP</a>
 

 

