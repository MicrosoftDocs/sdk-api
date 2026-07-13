---
UID: NS:winuser.tagEVENTMSG
title: EVENTMSG (winuser.h)
description: Contains information about a hardware message sent to the system message queue. This structure is used to store message information for the JournalPlaybackProc callback function.
helpviewer_keywords: ["*LPEVENTMSG","*LPEVENTMSGMSG","*NPEVENTMSG","*NPEVENTMSGMSG","*PEVENTMSG","*PEVENTMSGMSG","EVENTMSG","EVENTMSG structure [Windows and Messages]","LPEVENTMSG","LPEVENTMSG structure pointer [Windows and Messages]","PEVENTMSG","PEVENTMSG structure pointer [Windows and Messages]","_win32_EVENTMSG_str","_win32_eventmsg_str_cpp","winmsg.eventmsg","winui._win32_eventmsg_str","winuser/EVENTMSG","winuser/LPEVENTMSG","winuser/PEVENTMSG"]
old-location: winmsg\eventmsg.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookstructures\eventmsg.htm
ms.date: 12/05/2018
ms.keywords: '*LPEVENTMSG, *LPEVENTMSGMSG, *NPEVENTMSG, *NPEVENTMSGMSG, *PEVENTMSG, *PEVENTMSGMSG, EVENTMSG, EVENTMSG structure [Windows and Messages], LPEVENTMSG, LPEVENTMSG structure pointer [Windows and Messages], PEVENTMSG, PEVENTMSG structure pointer [Windows and Messages], _win32_EVENTMSG_str, _win32_eventmsg_str_cpp, winmsg.eventmsg, winui._win32_eventmsg_str, winuser/EVENTMSG, winuser/LPEVENTMSG, winuser/PEVENTMSG'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: EVENTMSG, *PEVENTMSGMSG, *NPEVENTMSGMSG, *LPEVENTMSGMSG, *PEVENTMSG, *NPEVENTMSG, *LPEVENTMSG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEVENTMSG
 - winuser/tagEVENTMSG
 - PEVENTMSGMSG
 - winuser/PEVENTMSGMSG
 - EVENTMSG
 - winuser/EVENTMSG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - EVENTMSG
---

# EVENTMSG structure


## -description

Contains information about a hardware message sent to the system message queue. This structure is used to store message information for the [JournalPlaybackProc](/windows/win32/winmsg/journalplaybackproc) callback function.

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



<a href="/windows/desktop/winmsg/hooks">Hooks</a>

[JournalPlaybackProc](/windows/win32/winmsg/journalplaybackproc)

<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowshookexa">SetWindowsHookEx</a>