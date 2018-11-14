---
UID: NS:wtsapi32._WTS_SESSION_INFOA
title: "_WTS_SESSION_INFOA"
author: windows-sdk-content
description: Contains information about a client session on a Remote Desktop Session Host (RD Session Host) server.
old-location: termserv\wts_session_info_str.htm
tech.root: termserv
ms.assetid: bb40d928-293a-4e2c-b7cf-2ac038da53c2
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*PWTS_SESSION_INFOA, PWTS_SESSION_INFO, PWTS_SESSION_INFO structure pointer [Remote Desktop Services], WTS_SESSION_INFO, WTS_SESSION_INFO structure [Remote Desktop Services], WTS_SESSION_INFOA, WTS_SESSION_INFOW, _WTS_SESSION_INFOA, _win32_wts_session_info_str, termserv.wts_session_info_str, wtsapi32/PWTS_SESSION_INFO, wtsapi32/WTS_SESSION_INFO, wtsapi32/WTS_SESSION_INFOA, wtsapi32/WTS_SESSION_INFOW"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: WTS_SESSION_INFOA, *PWTS_SESSION_INFOA
req.redist: 
---

# _WTS_SESSION_INFOA structure


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
      <a href="https://msdn.microsoft.com/ee376f5a-3474-4e31-94c1-e760346eb794">WTS_CONNECTSTATE_CLASS</a> enumeration type 
      that indicates the session's current connection state.


## -see-also




<a href="https://msdn.microsoft.com/6f9dd7d4-48dc-411c-85f1-cd1239d1e106">WTSEnumerateSessions</a>



<a href="https://msdn.microsoft.com/ee376f5a-3474-4e31-94c1-e760346eb794">WTS_CONNECTSTATE_CLASS</a>
 

 

