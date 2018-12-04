---
UID: NF:winuser.GetMessageTime
title: GetMessageTime function
author: windows-sdk-content
description: Retrieves the message time for the last message retrieved by the GetMessage function.
old-location: winmsg\getmessagetime.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\getmessagetime.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetMessageTime, GetMessageTime function [Windows and Messages], _win32_GetMessageTime, _win32_getmessagetime_cpp, winmsg.getmessagetime, winui._win32_getmessagetime, winuser/GetMessageTime
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
 - Ext-MS-Win-NTUser-message-l1-1-1.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - Ext-MS-Win-NTUser-Message-l1-1-2.dll
 - Ext-MS-Win-NTUser-Message-L1-1-3.dll
api_name:
 - GetMessageTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetMessageTime function


## -description


Retrieves the message time for the last message retrieved by the <a href="https://msdn.microsoft.com/e92266a7-86ac-43f4-b0eb-762e145a1017">GetMessage</a> function. The time is a long integer that specifies the elapsed time, in milliseconds, from the time the system was started to the time the message was created (that is, placed in the thread's message queue). 


## -parameters






## -returns



Type: <strong>Type: <b>LONG</b>
</strong>

The return value specifies the message time.




## -remarks



The return value from the <b>GetMessageTime</b> function does not necessarily increase between subsequent messages, because the value wraps to wraps to the minimum value for a long integer if the timer count exceeds the maximum value for a long integer.

To calculate time delays between messages, subtract the time of the first message from the time of the second message (ignoring overflow) and compare the result of the subtraction against the desired delay amount. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e92266a7-86ac-43f4-b0eb-762e145a1017">GetMessage</a>



<a href="https://msdn.microsoft.com/7244da5f-96f5-4cf6-acc3-697f8e4f7283">GetMessagePos</a>



<a href="https://msdn.microsoft.com/885bb607-3ec0-4e24-9f55-fbdfb1c538a1">Messages and Message Queues</a>



<b>Reference</b>
 

 

