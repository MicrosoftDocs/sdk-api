---
UID: NS:winuser.tagMSG
title: tagMSG
author: windows-sdk-content
description: Contains message information from a thread's message queue.
old-location: winmsg\msg.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messageandmessagequeuestructures\msg.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPMSG, *NPMSG, *PMSG, LPMSG, LPMSG structure pointer [Windows and Messages], MSG, MSG structure [Windows and Messages], PMSG, PMSG structure pointer [Windows and Messages], _win32_MSG_str, _win32_msg_str_cpp, tagMSG, winmsg.msg, winui._win32_msg_str, winuser/LPMSG, winuser/MSG, winuser/PMSG"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a></b>

The cursor position, in screen coordinates, when the message was posted. 


### -field lPrivate

 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e92266a7-86ac-43f4-b0eb-762e145a1017">GetMessage</a>



<a href="https://msdn.microsoft.com/885bb607-3ec0-4e24-9f55-fbdfb1c538a1">Messages and Message Queues</a>



<a href="https://msdn.microsoft.com/b9f5baa4-8166-4d6e-b416-df023aed9bad">PeekMessage</a>



<a href="https://msdn.microsoft.com/c418cb0e-1b9f-4ca8-8b02-e6901f7744a6">PostThreadMessage</a>



<b>Reference</b>
 

 

