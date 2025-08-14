---
UID: NF:winuser.SetMessageExtraInfo
title: SetMessageExtraInfo function (winuser.h)
description: Sets the extra message information for the current thread.
helpviewer_keywords: ["SetMessageExtraInfo","SetMessageExtraInfo function [Windows and Messages]","_win32_SetMessageExtraInfo","_win32_setmessageextrainfo_cpp","winmsg.setmessageextrainfo","winui._win32_setmessageextrainfo","winuser/SetMessageExtraInfo"]
old-location: winmsg\setmessageextrainfo.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\setmessageextrainfo.htm
ms.date: 12/05/2018
ms.keywords: SetMessageExtraInfo, SetMessageExtraInfo function [Windows and Messages], _win32_SetMessageExtraInfo, _win32_setmessageextrainfo_cpp, winmsg.setmessageextrainfo, winui._win32_setmessageextrainfo, winuser/SetMessageExtraInfo
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
 - SetMessageExtraInfo
 - winuser/SetMessageExtraInfo
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
 - ext-ms-win-ntuser-message-l1-1-3.dll
 - ext-ms-win-ntuser-message-l1-1-2.dll
 - ext-ms-win-ntuser-message-l1-1-1.dll
 - User32.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
api_name:
 - SetMessageExtraInfo
req.apiset: ext-ms-win-ntuser-message-l1-1-0 (introduced in Windows 8)
---

# SetMessageExtraInfo function


## -description

Sets the extra message information for the current thread. Extra message information is an application- or driver-defined value associated with the current thread's message queue. An application can use the <a href="/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo">GetMessageExtraInfo</a> function to retrieve a thread's extra message information.

## -parameters

### -param lParam [in]

Type: <b>LPARAM</b>

The value to be associated with the current thread.

## -returns

Type: <b>LPARAM</b>

The return value is the previous value associated with the current thread.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo">GetMessageExtraInfo</a>



<a href="/windows/desktop/winmsg/messages-and-message-queues">Messages and Message Queues</a>



<b>Reference</b>
