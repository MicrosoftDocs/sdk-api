---
UID: NS:winuser.tagMSG
title: tagMSG
author: windows-sdk-content
description: Contains message information from a thread's message queue.
old-location: winmsg\msg.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messageandmessagequeuestructures\msg.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*LPMSG, *NPMSG, *PMSG, LPMSG, LPMSG structure pointer [Windows and Messages], MSG, MSG structure [Windows and Messages], PMSG, PMSG structure pointer [Windows and Messages], _win32_MSG_str, _win32_msg_str_cpp, tagMSG, winmsg.msg, winui._win32_msg_str, winuser/LPMSG, winuser/MSG, winuser/PMSG"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.typenames: MSG, *PMSG, *NPMSG, *LPMSG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - MSG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagMSG structure


## -description


Contains message information from a thread's message queue. 


## -struct-fields




### -field hwnd

Type: <b>HWND</b>

A handle to the window whose window procedure receives the message. This member is <b>NULL</b> when the message is a thread message.


### -field message

Type: <b>UINT</b>

The message identifier. Applications can only use the low word; the high word is reserved by the system. 


### -field wParam

Type: <b>WPARAM</b>

Additional information about the message. The exact meaning depends on the value of the 
					<b>message</b> member. 


### -field lParam

Type: <b>LPARAM</b>

Additional information about the message. The exact meaning depends on the value of the 
					<b>message</b> member. 


### -field time

Type: <b>DWORD</b>

The time at which the message was posted. 


### -field pt

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a></b>

The cursor position, in screen coordinates, when the message was posted. 


### -field lPrivate

 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644936(v=VS.85).aspx">GetMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632590(v=VS.85).aspx">Messages and Message Queues</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644943(v=VS.85).aspx">PeekMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644946(v=VS.85).aspx">PostThreadMessage</a>



<b>Reference</b>
 

 

