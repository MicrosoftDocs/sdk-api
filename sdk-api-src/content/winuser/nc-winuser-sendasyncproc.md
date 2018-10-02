---
UID: NC:winuser.SENDASYNCPROC
title: SENDASYNCPROC
author: windows-sdk-content
description: An application-defined callback function used with the SendMessageCallback function.
old-location: winmsg\sendasyncproc.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\sendasyncproc.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SendAsyncProc, SendAsyncProc callback, SendAsyncProc callback function [Windows and Messages], _win32_SendAsyncProc, _win32_sendasyncproc_cpp, winmsg.sendasyncproc, winui._win32_sendasyncproc, winuser/SendAsyncProc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winuser.h
api_name:
 - SendAsyncProc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SENDASYNCPROC callback function


## -description


An application-defined callback function used with the <a href="https://msdn.microsoft.com/en-us/library/ms644951(v=VS.85).aspx">SendMessageCallback</a> function. The system passes the message to the callback function after passing the message to the destination window procedure. The <b>SENDASYNCPROC</b> type defines a pointer to this callback function. <i>SendAsyncProc</i> is a placeholder for the application-defined function name.


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3


### -param Arg4








#### - dwData [in]

Type: <b>ULONG_PTR</b>

An application-defined value sent from the <a href="https://msdn.microsoft.com/en-us/library/ms644951(v=VS.85).aspx">SendMessageCallback</a> function.


#### - hwnd [in]

Type: <b>HWND</b>

A handle to the window whose window procedure received the message. 

If the <a href="https://msdn.microsoft.com/en-us/library/ms644951(v=VS.85).aspx">SendMessageCallback</a> function was called with its <i>hwnd</i> parameter set to <b>HWND_BROADCAST</b>, the system calls the <i>SendAsyncProc</i> function once for each top-level window.


#### - lResult [in]

Type: <b>LRESULT</b>

The result of the message processing. This value depends on the message.


#### - uMsg [in]

Type: <b>UINT</b>

The message.


## -returns



This callback function does not return a value. 




## -remarks



You install a <i>SendAsyncProc</i> application-defined callback function by passing a <b>SENDASYNCPROC</b> pointer to the <a href="https://msdn.microsoft.com/en-us/library/ms644951(v=VS.85).aspx">SendMessageCallback</a> function. 

The callback function is only called when the thread that called <a href="https://msdn.microsoft.com/en-us/library/ms644951(v=VS.85).aspx">SendMessageCallback</a> calls <a href="https://msdn.microsoft.com/en-us/library/ms644936(v=VS.85).aspx">GetMessage</a>, <a href="https://msdn.microsoft.com/en-us/library/ms644943(v=VS.85).aspx">PeekMessage</a>, or <a href="https://msdn.microsoft.com/en-us/library/ms644956(v=VS.85).aspx">WaitMessage</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644936(v=VS.85).aspx">GetMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632590(v=VS.85).aspx">Messages and Message Queues</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644943(v=VS.85).aspx">PeekMessage</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644951(v=VS.85).aspx">SendMessageCallback</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644956(v=VS.85).aspx">WaitMessage</a>
 

 

