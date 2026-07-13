---
UID: NS:wtsapi32._WTS_SERVER_INFOW
title: WTS_SERVER_INFOW (wtsapi32.h)
description: Contains information about a specific Remote Desktop Services server. (Unicode)
helpviewer_keywords: ["*PWTS_SERVER_INFOW","PWTS_SERVER_INFO","PWTS_SERVER_INFO structure pointer [Remote Desktop Services]","WTS_SERVER_INFO","WTS_SERVER_INFO structure [Remote Desktop Services]","WTS_SERVER_INFOA","WTS_SERVER_INFOW","termserv.wts_server_info","wtsapi32/PWTS_SERVER_INFO","wtsapi32/WTS_SERVER_INFO","wtsapi32/WTS_SERVER_INFOA","wtsapi32/WTS_SERVER_INFOW"]
old-location: termserv\wts_server_info.htm
tech.root: TermServ
ms.assetid: c7ba5a94-37ff-408f-9a77-91b07c28b7ce
ms.date: 12/05/2018
ms.keywords: '*PWTS_SERVER_INFOW, PWTS_SERVER_INFO, PWTS_SERVER_INFO structure pointer [Remote Desktop Services], WTS_SERVER_INFO, WTS_SERVER_INFO structure [Remote Desktop Services], WTS_SERVER_INFOA, WTS_SERVER_INFOW, termserv.wts_server_info, wtsapi32/PWTS_SERVER_INFO, wtsapi32/WTS_SERVER_INFO, wtsapi32/WTS_SERVER_INFOA, wtsapi32/WTS_SERVER_INFOW'
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTS_SERVER_INFOW (Unicode) and WTS_SERVER_INFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WTS_SERVER_INFOW, *PWTS_SERVER_INFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WTS_SERVER_INFOW
 - wtsapi32/_WTS_SERVER_INFOW
 - PWTS_SERVER_INFOW
 - wtsapi32/PWTS_SERVER_INFOW
 - WTS_SERVER_INFOW
 - wtsapi32/WTS_SERVER_INFOW
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
 - WTS_SERVER_INFO
 - WTS_SERVER_INFOA
 - WTS_SERVER_INFOW
---

# WTS_SERVER_INFOW structure


## -description

Contains information about a specific Remote Desktop Services server.

## -struct-fields

### -field pServerName

Name of the server.

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsenumerateserversa">WTSEnumerateServers</a>

## -remarks

> [!NOTE]
> The wtsapi32.h header defines WTS_SERVER_INFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
