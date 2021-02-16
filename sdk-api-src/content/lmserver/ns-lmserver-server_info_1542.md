---
UID: NS:lmserver._SERVER_INFO_1542
title: SERVER_INFO_1542 (lmserver.h)
description: The SERVER_INFO_1542 structure specifies the maximum number of free connection blocks the server sets aside to handle bursts of requests by clients to connect to the server.
helpviewer_keywords: ["*LPSERVER_INFO_1542","*PSERVER_INFO_1542","LPSERVER_INFO_1542","LPSERVER_INFO_1542 structure pointer [Network Management]","PSERVER_INFO_1542","PSERVER_INFO_1542 structure pointer [Network Management]","SERVER_INFO_1542","SERVER_INFO_1542 structure [Network Management]","_win32_server_info_1542_str","lmserver/LPSERVER_INFO_1542","lmserver/PSERVER_INFO_1542","lmserver/SERVER_INFO_1542","netmgmt.server_info_1542_str"]
old-location: netmgmt\server_info_1542_str.htm
tech.root: NetMgmt
ms.assetid: 49c38acd-ed20-4ddc-a97a-9d77b8907378
ms.date: 12/05/2018
ms.keywords: '*LPSERVER_INFO_1542, *PSERVER_INFO_1542, LPSERVER_INFO_1542, LPSERVER_INFO_1542 structure pointer [Network Management], PSERVER_INFO_1542, PSERVER_INFO_1542 structure pointer [Network Management], SERVER_INFO_1542, SERVER_INFO_1542 structure [Network Management], _win32_server_info_1542_str, lmserver/LPSERVER_INFO_1542, lmserver/PSERVER_INFO_1542, lmserver/SERVER_INFO_1542, netmgmt.server_info_1542_str'
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
req.typenames: SERVER_INFO_1542, *PSERVER_INFO_1542, *LPSERVER_INFO_1542
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVER_INFO_1542
 - lmserver/_SERVER_INFO_1542
 - PSERVER_INFO_1542
 - lmserver/PSERVER_INFO_1542
 - SERVER_INFO_1542
 - lmserver/SERVER_INFO_1542
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
 - SERVER_INFO_1542
---

# SERVER_INFO_1542 structure


## -description

The
				<b>SERVER_INFO_1542</b> structure specifies the maximum number of free connection blocks the server sets aside to handle bursts of requests by clients to connect to the server.

## -struct-fields

### -field sv1542_maxfreeconnections

Specifies the maximum number of free connection blocks maintained per endpoint. The server sets these aside to handle bursts of requests by clients to connect to the server.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/server-functions">Server Functions</a>