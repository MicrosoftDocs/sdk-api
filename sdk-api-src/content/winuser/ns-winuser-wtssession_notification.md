---
UID: NS:winuser.tagWTSSESSION_NOTIFICATION
title: WTSSESSION_NOTIFICATION (winuser.h)
description: Provides information about the session change notification. A service receives this structure in its HandlerEx function in response to a session change event.
helpviewer_keywords: ["*PWTSSESSION_NOTIFICATION","PWTSSESSION_NOTIFICATION","PWTSSESSION_NOTIFICATION structure pointer [Remote Desktop Services]","WTSSESSION_NOTIFICATION","WTSSESSION_NOTIFICATION structure [Remote Desktop Services]","_win32_wtssession_notification_str","termserv.wtssession_notification_str","winuser/PWTSSESSION_NOTIFICATION","winuser/WTSSESSION_NOTIFICATION"]
old-location: termserv\wtssession_notification_str.htm
tech.root: TermServ
ms.assetid: 863bd689-796b-4875-81bf-f853354b08b5
ms.date: 12/05/2018
ms.keywords: '*PWTSSESSION_NOTIFICATION, PWTSSESSION_NOTIFICATION, PWTSSESSION_NOTIFICATION structure pointer [Remote Desktop Services], WTSSESSION_NOTIFICATION, WTSSESSION_NOTIFICATION structure [Remote Desktop Services], _win32_wtssession_notification_str, termserv.wtssession_notification_str, winuser/PWTSSESSION_NOTIFICATION, winuser/WTSSESSION_NOTIFICATION'
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: WTSSESSION_NOTIFICATION, *PWTSSESSION_NOTIFICATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWTSSESSION_NOTIFICATION
 - winuser/tagWTSSESSION_NOTIFICATION
 - PWTSSESSION_NOTIFICATION
 - winuser/PWTSSESSION_NOTIFICATION
 - WTSSESSION_NOTIFICATION
 - winuser/WTSSESSION_NOTIFICATION
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
 - WTSSESSION_NOTIFICATION
---

# WTSSESSION_NOTIFICATION structure


## -description

Provides information about the session change notification. A service receives this structure in its 
    <a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex">HandlerEx</a> function in response to a session change event.

## -struct-fields

### -field cbSize

Size, in bytes, of this structure.

### -field dwSessionId

Session identifier that triggered the session change event.

## -see-also

<a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex">HandlerEx</a>