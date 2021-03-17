---
UID: NS:lmserver._SERVER_INFO_1510
title: SERVER_INFO_1510 (lmserver.h)
description: The SERVER_INFO_1510 structure specifies the maximum number of users that can be logged on to the specified server using a single virtual circuit.
helpviewer_keywords: ["*LPSERVER_INFO_1510","*PSERVER_INFO_1510","LPSERVER_INFO_1510","LPSERVER_INFO_1510 structure pointer [Network Management]","PSERVER_INFO_1510","PSERVER_INFO_1510 structure pointer [Network Management]","SERVER_INFO_1510","SERVER_INFO_1510 structure [Network Management]","_win32_server_info_1510_str","lmserver/LPSERVER_INFO_1510","lmserver/PSERVER_INFO_1510","lmserver/SERVER_INFO_1510","netmgmt.server_info_1510_str"]
old-location: netmgmt\server_info_1510_str.htm
tech.root: NetMgmt
ms.assetid: 4bef21e3-09b9-4045-b21f-6cb9a75e2ad4
ms.date: 12/05/2018
ms.keywords: '*LPSERVER_INFO_1510, *PSERVER_INFO_1510, LPSERVER_INFO_1510, LPSERVER_INFO_1510 structure pointer [Network Management], PSERVER_INFO_1510, PSERVER_INFO_1510 structure pointer [Network Management], SERVER_INFO_1510, SERVER_INFO_1510 structure [Network Management], _win32_server_info_1510_str, lmserver/LPSERVER_INFO_1510, lmserver/PSERVER_INFO_1510, lmserver/SERVER_INFO_1510, netmgmt.server_info_1510_str'
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
req.typenames: SERVER_INFO_1510, *PSERVER_INFO_1510, *LPSERVER_INFO_1510
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVER_INFO_1510
 - lmserver/_SERVER_INFO_1510
 - PSERVER_INFO_1510
 - lmserver/PSERVER_INFO_1510
 - SERVER_INFO_1510
 - lmserver/SERVER_INFO_1510
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
 - SERVER_INFO_1510
---

# SERVER_INFO_1510 structure


## -description

The
				<b>SERVER_INFO_1510</b> structure specifies the maximum number of users that can be logged on to the specified server using a single virtual circuit.

## -struct-fields

### -field sv1510_sessusers

Specifies the maximum number of users that can be logged on to a server using a single virtual circuit.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/server-functions">Server Functions</a>