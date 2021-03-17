---
UID: NS:lmserver._SERVER_INFO_1544
title: SERVER_INFO_1544 (lmserver.h)
description: The SERVER_INFO_1544 structure specifies the initial number of tree connections to be allocated in the connection table.
helpviewer_keywords: ["*LPSERVER_INFO_1544","*PSERVER_INFO_1544","LPSERVER_INFO_1544","LPSERVER_INFO_1544 structure pointer [Network Management]","PSERVER_INFO_1544","PSERVER_INFO_1544 structure pointer [Network Management]","SERVER_INFO_1544","SERVER_INFO_1544 structure [Network Management]","_win32_server_info_1544_str","lmserver/LPSERVER_INFO_1544","lmserver/PSERVER_INFO_1544","lmserver/SERVER_INFO_1544","netmgmt.server_info_1544_str"]
old-location: netmgmt\server_info_1544_str.htm
tech.root: NetMgmt
ms.assetid: 11a985b0-b092-44f0-83b9-4628a01db00e
ms.date: 12/05/2018
ms.keywords: '*LPSERVER_INFO_1544, *PSERVER_INFO_1544, LPSERVER_INFO_1544, LPSERVER_INFO_1544 structure pointer [Network Management], PSERVER_INFO_1544, PSERVER_INFO_1544 structure pointer [Network Management], SERVER_INFO_1544, SERVER_INFO_1544 structure [Network Management], _win32_server_info_1544_str, lmserver/LPSERVER_INFO_1544, lmserver/PSERVER_INFO_1544, lmserver/SERVER_INFO_1544, netmgmt.server_info_1544_str'
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
req.typenames: SERVER_INFO_1544, *PSERVER_INFO_1544, *LPSERVER_INFO_1544
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVER_INFO_1544
 - lmserver/_SERVER_INFO_1544
 - PSERVER_INFO_1544
 - lmserver/PSERVER_INFO_1544
 - SERVER_INFO_1544
 - lmserver/SERVER_INFO_1544
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
 - SERVER_INFO_1544
---

# SERVER_INFO_1544 structure


## -description

The
				<b>SERVER_INFO_1544</b> structure specifies the initial number of tree connections to be allocated in the connection table.

## -struct-fields

### -field sv1544_initconntable

Specifies the initial number of tree connections to be allocated in the connection table. The server automatically increases the table as necessary, so setting the member to a higher value is an optimization.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/server-functions">Server Functions</a>