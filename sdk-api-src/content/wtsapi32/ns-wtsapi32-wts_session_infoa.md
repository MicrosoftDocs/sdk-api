---
UID: NS:wtsapi32._WTS_SESSION_INFOA
title: WTS_SESSION_INFOA (wtsapi32.h)
description: Contains information about a client session on a Remote Desktop Session Host (RD Session Host) server. (ANSI)
helpviewer_keywords: ["*PWTS_SESSION_INFOA","PWTS_SESSION_INFO","PWTS_SESSION_INFO structure pointer [Remote Desktop Services]","WTS_SESSION_INFO","WTS_SESSION_INFO structure [Remote Desktop Services]","WTS_SESSION_INFOA","WTS_SESSION_INFOW","_win32_wts_session_info_str","termserv.wts_session_info_str","wtsapi32/PWTS_SESSION_INFO","wtsapi32/WTS_SESSION_INFO","wtsapi32/WTS_SESSION_INFOA","wtsapi32/WTS_SESSION_INFOW"]
old-location: termserv\wts_session_info_str.htm
tech.root: TermServ
ms.assetid: bb40d928-293a-4e2c-b7cf-2ac038da53c2
ms.date: 12/05/2018
ms.keywords: '*PWTS_SESSION_INFOA, PWTS_SESSION_INFO, PWTS_SESSION_INFO structure pointer [Remote Desktop Services], WTS_SESSION_INFO, WTS_SESSION_INFO structure [Remote Desktop Services], WTS_SESSION_INFOA, WTS_SESSION_INFOW, _win32_wts_session_info_str, termserv.wts_session_info_str, wtsapi32/PWTS_SESSION_INFO, wtsapi32/WTS_SESSION_INFO, wtsapi32/WTS_SESSION_INFOA, wtsapi32/WTS_SESSION_INFOW'
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTS_SESSION_INFOW (Unicode) and WTS_SESSION_INFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WTS_SESSION_INFOA, *PWTS_SESSION_INFOA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WTS_SESSION_INFOA
 - wtsapi32/_WTS_SESSION_INFOA
 - PWTS_SESSION_INFOA
 - wtsapi32/PWTS_SESSION_INFOA
 - WTS_SESSION_INFOA
 - wtsapi32/WTS_SESSION_INFOA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsapi32.h
api_name:
 - WTS_SESSION_INFO
 - WTS_SESSION_INFOA
 - WTS_SESSION_INFOW
---

# WTS_SESSION_INFOA structure


## -description

Contains 
    information about a client session on a Remote Desktop Session Host (RD Session Host) server.

## -struct-fields

### -field SessionId

Session identifier of the session.

### -field pWinStationName

Pointer to a null-terminated string that contains the WinStation name of this session. The WinStation name is a name that Windows associates with the session, for example, "services", "console", or "RDP-Tcp#0".

### -field State

A value from the 
      <a href="/windows/desktop/api/wtsapi32/ne-wtsapi32-wts_connectstate_class">WTS_CONNECTSTATE_CLASS</a> enumeration type 
      that indicates the session's current connection state.

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa">WTSEnumerateSessions</a>



<a href="/windows/desktop/api/wtsapi32/ne-wtsapi32-wts_connectstate_class">WTS_CONNECTSTATE_CLASS</a>

## -remarks

> [!NOTE]
> The wtsapi32.h header defines WTS_SESSION_INFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
