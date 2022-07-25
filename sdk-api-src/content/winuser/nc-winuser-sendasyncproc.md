---
UID: NC:winuser.SENDASYNCPROC
title: SENDASYNCPROC (winuser.h)
description: An application-defined callback function used with the SendMessageCallback function.
helpviewer_keywords: ["SendAsyncProc","SendAsyncProc callback","SendAsyncProc callback function [Windows and Messages]","_win32_SendAsyncProc","_win32_sendasyncproc_cpp","winmsg.sendasyncproc","winui._win32_sendasyncproc","winuser/SendAsyncProc"]
old-location: winmsg\sendasyncproc.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\sendasyncproc.htm
ms.date: 12/05/2018
ms.keywords: SendAsyncProc, SendAsyncProc callback, SendAsyncProc callback function [Windows and Messages], _win32_SendAsyncProc, _win32_sendasyncproc_cpp, winmsg.sendasyncproc, winui._win32_sendasyncproc, winuser/SendAsyncProc
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SENDASYNCPROC
 - winuser/SENDASYNCPROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winuser.h
api_name:
 - SendAsyncProc
---

# SENDASYNCPROC callback function


## -description

An application-defined callback function used with the <a href="/windows/desktop/api/winuser/nf-winuser-sendmessagecallbacka">SendMessageCallback</a> function. The system passes the message to the callback function after passing the message to the destination window procedure. The <b>SENDASYNCPROC</b> type defines a pointer to this callback function. <i>SendAsyncProc</i> is a placeholder for the application-defined function name.

## -parameters

### -param unnamedParam1

Type: <b>HWND</b>

A handle to the window whose window procedure received the message. 

If the <a href="/windows/desktop/api/winuser/nf-winuser-sendmessagecallbacka">SendMessageCallback</a> function was called with its <i>hwnd</i> parameter set to <b>HWND_BROADCAST</b>, the system calls the <i>SendAsyncProc</i> function once for each top-level window.

### -param unnamedParam2

Type: <b>UINT</b>

The message.

### -param unnamedParam3

Type: <b>ULONG_PTR</b>

An application-defined value sent from the <a href="/windows/desktop/api/winuser/nf-winuser-sendmessagecallbacka">SendMessageCallback</a> function.

### -param unnamedParam4

Type: <b>LRESULT</b>

The result of the message processing. This value depends on the message.

## -remarks

You install a <i>SendAsyncProc</i> application-defined callback function by passing a <b>SENDASYNCPROC</b> pointer to the <a href="/windows/desktop/api/winuser/nf-winuser-sendmessagecallbacka">SendMessageCallback</a> function. 

The callback function is only called when the thread that called <a href="/windows/desktop/api/winuser/nf-winuser-sendmessagecallbacka">SendMessageCallback</a> calls <a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>, <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>, or <a href="/windows/desktop/api/winuser/nf-winuser-waitmessage">WaitMessage</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>



<a href="/windows/desktop/winmsg/messages-and-message-queues">Messages and Message Queues</a>



<a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-sendmessagecallbacka">SendMessageCallback</a>



<a href="/windows/desktop/api/winuser/nf-winuser-waitmessage">WaitMessage</a>