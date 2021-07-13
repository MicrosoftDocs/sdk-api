---
UID: NF:winuser.GetInputState
title: GetInputState function (winuser.h)
description: Determines whether there are mouse-button or keyboard messages in the calling thread's message queue.
helpviewer_keywords: ["GetInputState","GetInputState function [Windows and Messages]","_win32_GetInputState","_win32_getinputstate_cpp","winmsg.getinputstate","winui._win32_getinputstate","winuser/GetInputState"]
old-location: winmsg\getinputstate.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\getinputstate.htm
ms.date: 12/05/2018
ms.keywords: GetInputState, GetInputState function [Windows and Messages], _win32_GetInputState, _win32_getinputstate_cpp, winmsg.getinputstate, winui._win32_getinputstate, winuser/GetInputState
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetInputState
 - winuser/GetInputState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - GetInputState
---

# GetInputState function


## -description

Determines whether there are mouse-button or keyboard messages in the calling thread's message queue.



## -returns

Type: <b>BOOL</b>

If the queue contains one or more new mouse-button or keyboard messages, the return value is nonzero.

If there are no new mouse-button or keyboard messages in the queue, the return value is zero.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getqueuestatus">GetQueueStatus</a>



<a href="/windows/desktop/winmsg/messages-and-message-queues">Messages and Message Queues</a>



<b>Reference</b>
