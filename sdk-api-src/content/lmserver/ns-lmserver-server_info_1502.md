---
UID: NS:lmserver._SERVER_INFO_1502
title: SERVER_INFO_1502 (lmserver.h)
description: The SERVER_INFO_1502 structure specifies the maximum number of virtual circuits per client for the specified server.
helpviewer_keywords: ["*LPSERVER_INFO_1502","*PSERVER_INFO_1502","LPSERVER_INFO_1502","LPSERVER_INFO_1502 structure pointer [Network Management]","PSERVER_INFO_1502","PSERVER_INFO_1502 structure pointer [Network Management]","SERVER_INFO_1502","SERVER_INFO_1502 structure [Network Management]","_win32_server_info_1502_str","lmserver/LPSERVER_INFO_1502","lmserver/PSERVER_INFO_1502","lmserver/SERVER_INFO_1502","netmgmt.server_info_1502_str"]
old-location: netmgmt\server_info_1502_str.htm
tech.root: NetMgmt
ms.assetid: d33cfe93-b284-4299-82fd-8055b39f7b87
ms.date: 12/05/2018
ms.keywords: '*LPSERVER_INFO_1502, *PSERVER_INFO_1502, LPSERVER_INFO_1502, LPSERVER_INFO_1502 structure pointer [Network Management], PSERVER_INFO_1502, PSERVER_INFO_1502 structure pointer [Network Management], SERVER_INFO_1502, SERVER_INFO_1502 structure [Network Management], _win32_server_info_1502_str, lmserver/LPSERVER_INFO_1502, lmserver/PSERVER_INFO_1502, lmserver/SERVER_INFO_1502, netmgmt.server_info_1502_str'
req.header: lmserver.h
req.include-header: Lm.h
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
req.typenames: SERVER_INFO_1502, *PSERVER_INFO_1502, *LPSERVER_INFO_1502
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVER_INFO_1502
 - lmserver/_SERVER_INFO_1502
 - PSERVER_INFO_1502
 - lmserver/PSERVER_INFO_1502
 - SERVER_INFO_1502
 - lmserver/SERVER_INFO_1502
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmserver.h
api_name:
 - SERVER_INFO_1502
---

# SERVER_INFO_1502 structure


## -description

The
				<b>SERVER_INFO_1502</b> structure specifies the maximum number of virtual circuits per client for the specified server.

## -struct-fields

### -field sv1502_sessvcs

Specifies the maximum number of virtual circuits permitted per client.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/server-functions">Server Functions</a>