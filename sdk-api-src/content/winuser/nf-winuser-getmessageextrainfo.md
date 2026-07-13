---
UID: NF:winuser.GetMessageExtraInfo
title: GetMessageExtraInfo function (winuser.h)
description: Retrieves the extra message information for the current thread. Extra message information is an application- or driver-defined value associated with the current thread's message queue.
helpviewer_keywords: ["GetMessageExtraInfo","GetMessageExtraInfo function [Windows and Messages]","_win32_GetMessageExtraInfo","_win32_getmessageextrainfo_cpp","winmsg.getmessageextrainfo","winui._win32_getmessageextrainfo","winuser/GetMessageExtraInfo"]
old-location: winmsg\getmessageextrainfo.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\getmessageextrainfo.htm
ms.date: 12/05/2018
ms.keywords: GetMessageExtraInfo, GetMessageExtraInfo function [Windows and Messages], _win32_GetMessageExtraInfo, _win32_getmessageextrainfo_cpp, winmsg.getmessageextrainfo, winui._win32_getmessageextrainfo, winuser/GetMessageExtraInfo
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
 - GetMessageExtraInfo
 - winuser/GetMessageExtraInfo
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
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
 - API-MS-Win-NTUser-IE-message-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
api_name:
 - GetMessageExtraInfo
req.apiset: ext-ms-win-ntuser-window-l1-1-4 (introduced in Windows 10, version 10.0.14393)
---

# GetMessageExtraInfo function


## -description

Retrieves the extra message information for the current thread. Extra message information is an application- or driver-defined value associated with the current thread's message queue.



## -returns

Type: <b>LPARAM</b>

The return value specifies the extra information. The meaning of the extra information is device specific.

## -remarks

To set a thread's extra message information, use the <a href="/windows/desktop/api/winuser/nf-winuser-setmessageextrainfo">SetMessageExtraInfo</a> function.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>



<a href="/windows/desktop/winmsg/messages-and-message-queues">Messages and Message Queues</a>



<a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setmessageextrainfo">SetMessageExtraInfo</a>
