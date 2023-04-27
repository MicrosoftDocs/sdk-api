---
UID: NS:winuser.BSMINFO
title: BSMINFO (winuser.h)
description: Contains information about a window that denied a request from BroadcastSystemMessageEx.
helpviewer_keywords: ["*PBSMINFO","BSMINFO","BSMINFO structure [Windows and Messages]","PBSMINFO","PBSMINFO structure pointer [Windows and Messages]","_win32_BSMINFO_str","_win32_bsminfo_str_cpp","winmsg.bsminfo","winui._win32_bsminfo_str","winuser/BSMINFO","winuser/PBSMINFO"]
old-location: winmsg\bsminfo.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messageandmessagequeuestructures\bsminfo.htm
ms.date: 12/05/2018
ms.keywords: '*PBSMINFO, BSMINFO, BSMINFO structure [Windows and Messages], PBSMINFO, PBSMINFO structure pointer [Windows and Messages], _win32_BSMINFO_str, _win32_bsminfo_str_cpp, winmsg.bsminfo, winui._win32_bsminfo_str, winuser/BSMINFO, winuser/PBSMINFO'
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: BSMINFO, *PBSMINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PBSMINFO
 - winuser/PBSMINFO
 - BSMINFO
 - winuser/BSMINFO
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
 - BSMINFO
---

# BSMINFO structure


## -description

Contains information about a window that denied a request from <a href="/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessageexa">BroadcastSystemMessageEx</a>.

## -struct-fields

### -field cbSize

Type: <b>UINT</b>

The size, in bytes, of this structure.

### -field hdesk

Type: <b>HDESK</b>

A desktop handle to the window specified by 
					<b>hwnd</b>. This value is returned only if <a href="/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessageexa">BroadcastSystemMessageEx</a> specifies <b>BSF_RETURNHDESK</b> and <b>BSF_QUERY</b>.

### -field hwnd

Type: <b>HWND</b>

A handle to the window that denied the request. This value is returned if <a href="/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessageexa">BroadcastSystemMessageEx</a> specifies <b>BSF_QUERY</b>.

### -field luid

Type: <b>LUID</b>

A locally unique identifier (LUID) for the window.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessageexa">BroadcastSystemMessageEx</a>



<b>Conceptual</b>



<a href="/windows/desktop/winmsg/messages-and-message-queues">Messages and Message Queues</a>



<b>Reference</b>

