---
UID: NS:winuser.tagEVENTMSG
title: tagEVENTMSG
author: windows-sdk-content
description: Contains information about a hardware message sent to the system message queue. This structure is used to store message information for the JournalPlaybackProc callback function.
old-location: winmsg\eventmsg.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookstructures\eventmsg.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPEVENTMSG, *LPEVENTMSGMSG, *NPEVENTMSG, *NPEVENTMSGMSG, *PEVENTMSG, *PEVENTMSGMSG, EVENTMSG, EVENTMSG structure [Windows and Messages], LPEVENTMSG, LPEVENTMSG structure pointer [Windows and Messages], PEVENTMSG, PEVENTMSG structure pointer [Windows and Messages], _win32_EVENTMSG_str, _win32_eventmsg_str_cpp, tagEVENTMSG, winmsg.eventmsg, winui._win32_eventmsg_str, winuser/EVENTMSG, winuser/LPEVENTMSG, winuser/PEVENTMSG"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: EVENTMSG, *PEVENTMSGMSG, *NPEVENTMSGMSG, *LPEVENTMSGMSG, *PEVENTMSG, *NPEVENTMSG, *LPEVENTMSG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - EVENTMSG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagEVENTMSG structure


## -description


Contains information about a hardware message sent to the system message queue. This structure is used to store message information for the <a href="https://msdn.microsoft.com/en-us/library/ms644982(v=VS.85).aspx">JournalPlaybackProc</a> callback function. 


## -struct-fields




### -field message

Type: <b>UINT</b>

The message. 


### -field paramL

Type: <b>UINT</b>

Additional information about the message. The exact meaning depends on the 
					<b>message</b> value. 


### -field paramH

Type: <b>UINT</b>

Additional information about the message. The exact meaning depends on the 
					<b>message</b> value. 


### -field time

Type: <b>DWORD</b>

The time at which the message was posted. 


### -field hwnd

Type: <b>HWND</b>

A handle to the window to which the message was posted. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632589(v=VS.85).aspx">Hooks</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644982(v=VS.85).aspx">JournalPlaybackProc</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644990(v=VS.85).aspx">SetWindowsHookEx</a>
 

 

