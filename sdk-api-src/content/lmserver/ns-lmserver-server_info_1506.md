---
UID: NS:lmserver._SERVER_INFO_1506
title: SERVER_INFO_1506 (lmserver.h)
description: The SERVER_INFO_1506 structure contains information about the maximum number of work items the specified server can allocate.
helpviewer_keywords: ["*LPSERVER_INFO_1506","*PSERVER_INFO_1506","LPSERVER_INFO_1506","LPSERVER_INFO_1506 structure pointer [Network Management]","PSERVER_INFO_1506","PSERVER_INFO_1506 structure pointer [Network Management]","SERVER_INFO_1506","SERVER_INFO_1506 structure [Network Management]","_win32_server_info_1506_str","lmserver/LPSERVER_INFO_1506","lmserver/PSERVER_INFO_1506","lmserver/SERVER_INFO_1506","netmgmt.server_info_1506_str"]
old-location: netmgmt\server_info_1506_str.htm
tech.root: NetMgmt
ms.assetid: 3a18838b-2a47-4b78-9356-f20de8a87d2f
ms.date: 12/05/2018
ms.keywords: '*LPSERVER_INFO_1506, *PSERVER_INFO_1506, LPSERVER_INFO_1506, LPSERVER_INFO_1506 structure pointer [Network Management], PSERVER_INFO_1506, PSERVER_INFO_1506 structure pointer [Network Management], SERVER_INFO_1506, SERVER_INFO_1506 structure [Network Management], _win32_server_info_1506_str, lmserver/LPSERVER_INFO_1506, lmserver/PSERVER_INFO_1506, lmserver/SERVER_INFO_1506, netmgmt.server_info_1506_str'
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
req.typenames: SERVER_INFO_1506, *PSERVER_INFO_1506, *LPSERVER_INFO_1506
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVER_INFO_1506
 - lmserver/_SERVER_INFO_1506
 - PSERVER_INFO_1506
 - lmserver/PSERVER_INFO_1506
 - SERVER_INFO_1506
 - lmserver/SERVER_INFO_1506
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
 - SERVER_INFO_1506
---

# SERVER_INFO_1506 structure


## -description

The
				<b>SERVER_INFO_1506</b> structure contains information about the maximum number of work items the specified server can allocate.

## -struct-fields

### -field sv1506_maxworkitems

Specifies the maximum number of receive buffers, or work items, the server can allocate. If this limit is reached, the transport protocol must initiate flow control at a significant cost to performance.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/server-functions">Server Functions</a>