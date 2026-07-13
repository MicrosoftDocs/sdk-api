---
UID: NF:winuser.GetMessageTime
title: GetMessageTime function (winuser.h)
description: Retrieves the message time for the last message retrieved by the GetMessage function.
helpviewer_keywords: ["GetMessageTime","GetMessageTime function [Windows and Messages]","_win32_GetMessageTime","_win32_getmessagetime_cpp","winmsg.getmessagetime","winui._win32_getmessagetime","winuser/GetMessageTime"]
old-location: winmsg\getmessagetime.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\getmessagetime.htm
ms.date: 12/05/2018
ms.keywords: GetMessageTime, GetMessageTime function [Windows and Messages], _win32_GetMessageTime, _win32_getmessagetime_cpp, winmsg.getmessagetime, winui._win32_getmessagetime, winuser/GetMessageTime
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
 - GetMessageTime
 - winuser/GetMessageTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-window-ext-l1-1-1.dll
 - ext-ms-win-rtcore-ntuser-message-l1-1-0.dll
 - User32.dll
 - API-MS-Win-NTUser-IE-message-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-message-l1-1-1.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - Ext-MS-Win-NTUser-Message-l1-1-2.dll
 - Ext-MS-Win-NTUser-Message-L1-1-3.dll
api_name:
 - GetMessageTime
req.apiset: ext-ms-win-ntuser-message-l1-1-1 (introduced in Windows 8.1)
---

# GetMessageTime function


## -description

Retrieves the message time for the last message retrieved by the <a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a> function. The time is a long integer that specifies the elapsed time, in milliseconds, from the time the system was started to the time the message was created (that is, placed in the thread's message queue).



## -returns

Type: <b>LONG</b>

The return value specifies the message time.

## -remarks

The return value from the <b>GetMessageTime</b> function does not necessarily increase between subsequent messages, because the value wraps to the minimum value for a long integer if the timer count exceeds the maximum value for a long integer.

To calculate time delays between messages, subtract the time of the first message from the time of the second message (ignoring overflow) and compare the result of the subtraction against the desired delay amount.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getmessagepos">GetMessagePos</a>



<a href="/windows/desktop/winmsg/messages-and-message-queues">Messages and Message Queues</a>



<b>Reference</b>
