---
UID: NF:winuser.SetMessageExtraInfo
title: SetMessageExtraInfo function
author: windows-sdk-content
description: Sets the extra message information for the current thread.
old-location: winmsg\setmessageextrainfo.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\setmessageextrainfo.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SetMessageExtraInfo, SetMessageExtraInfo function [Windows and Messages], _win32_SetMessageExtraInfo, _win32_setmessageextrainfo_cpp, winmsg.setmessageextrainfo, winui._win32_setmessageextrainfo, winuser/SetMessageExtraInfo
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
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
api_name:
 - SetMessageExtraInfo
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetMessageExtraInfo function


## -description


Sets the extra message information for the current thread. Extra message information is an application- or driver-defined value associated with the current thread's message queue. An application can use the <a href="https://msdn.microsoft.com/c2b978b4-165b-44a0-8091-580e82f7e310">GetMessageExtraInfo</a> function to retrieve a thread's extra message information.


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



<a href="https://msdn.microsoft.com/c2b978b4-165b-44a0-8091-580e82f7e310">GetMessageExtraInfo</a>



<a href="https://msdn.microsoft.com/885bb607-3ec0-4e24-9f55-fbdfb1c538a1">Messages and Message Queues</a>



<b>Reference</b>
 

 

