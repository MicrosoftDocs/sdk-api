---
UID: NF:winuser.GetMessageExtraInfo
title: GetMessageExtraInfo function
author: windows-sdk-content
description: Retrieves the extra message information for the current thread. Extra message information is an application- or driver-defined value associated with the current thread's message queue.
old-location: winmsg\getmessageextrainfo.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\getmessageextrainfo.htm
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: GetMessageExtraInfo, GetMessageExtraInfo function [Windows and Messages], _win32_GetMessageExtraInfo, _win32_getmessageextrainfo_cpp, winmsg.getmessageextrainfo, winui._win32_getmessageextrainfo, winuser/GetMessageExtraInfo
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
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
api_name:
 - GetMessageExtraInfo
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetMessageExtraInfo function


## -description


Retrieves the extra message information for the current thread. Extra message information is an application- or driver-defined value associated with the current thread's message queue. 


## -parameters






## -returns



Type: <strong>Type: <b>LPARAM</b>
</strong>

The return value specifies the extra information. The meaning of the extra information is device specific.




## -remarks



To set a thread's extra message information, use the <a href="https://msdn.microsoft.com/library/ms644954(v=VS.85).aspx">SetMessageExtraInfo</a> function. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/ms644936(v=VS.85).aspx">GetMessage</a>



<a href="https://msdn.microsoft.com/library/ms632590(v=VS.85).aspx">Messages and Message Queues</a>



<a href="https://msdn.microsoft.com/library/ms644943(v=VS.85).aspx">PeekMessage</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/ms644954(v=VS.85).aspx">SetMessageExtraInfo</a>
 

 

