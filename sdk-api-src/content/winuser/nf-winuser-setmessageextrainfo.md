---
UID: NF:winuser.SetMessageExtraInfo
title: SetMessageExtraInfo function (winuser.h)
author: windows-sdk-content
description: Sets the extra message information for the current thread.
old-location: winmsg\setmessageextrainfo.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\setmessageextrainfo.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetMessageExtraInfo, SetMessageExtraInfo function [Windows and Messages], _win32_SetMessageExtraInfo, _win32_setmessageextrainfo_cpp, winmsg.setmessageextrainfo, winui._win32_setmessageextrainfo, winuser/SetMessageExtraInfo
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
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
api_name:
 - SetMessageExtraInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetMessageExtraInfo function


## -description


Sets the extra message information for the current thread. Extra message information is an application- or driver-defined value associated with the current thread's message queue. An application can use the <a href="https://msdn.microsoft.com/en-us/library/ms644937(v=VS.85).aspx">GetMessageExtraInfo</a> function to retrieve a thread's extra message information.


## -parameters




### -param lParam [in]

Type: <b>LPARAM</b>

The value to be associated with the current thread.


## -returns



Type: <strong>Type: <b>LPARAM</b>
</strong>

The return value is the previous value associated with the current thread.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644937(v=VS.85).aspx">GetMessageExtraInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632590(v=VS.85).aspx">Messages and Message Queues</a>



<b>Reference</b>
 

 

