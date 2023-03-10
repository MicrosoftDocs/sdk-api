---
UID: NS:lmserver._SERVER_INFO_1530
title: SERVER_INFO_1530 (lmserver.h)
description: The SERVER_INFO_1530 structure specifies the minimum number of available receive work items the server requires to begin processing a server message block.
helpviewer_keywords: ["*LPSERVER_INFO_1530","*PSERVER_INFO_1530","LPSERVER_INFO_1530","LPSERVER_INFO_1530 structure pointer [Network Management]","PSERVER_INFO_1530","PSERVER_INFO_1530 structure pointer [Network Management]","SERVER_INFO_1530","SERVER_INFO_1530 structure [Network Management]","_win32_server_info_1530_str","lmserver/LPSERVER_INFO_1530","lmserver/PSERVER_INFO_1530","lmserver/SERVER_INFO_1530","netmgmt.server_info_1530_str"]
old-location: netmgmt\server_info_1530_str.htm
tech.root: NetMgmt
ms.assetid: 972c69e6-9f9c-49c2-a799-7b72dd8aa696
ms.date: 12/05/2018
ms.keywords: '*LPSERVER_INFO_1530, *PSERVER_INFO_1530, LPSERVER_INFO_1530, LPSERVER_INFO_1530 structure pointer [Network Management], PSERVER_INFO_1530, PSERVER_INFO_1530 structure pointer [Network Management], SERVER_INFO_1530, SERVER_INFO_1530 structure [Network Management], _win32_server_info_1530_str, lmserver/LPSERVER_INFO_1530, lmserver/PSERVER_INFO_1530, lmserver/SERVER_INFO_1530, netmgmt.server_info_1530_str'
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
req.typenames: SERVER_INFO_1530, *PSERVER_INFO_1530, *LPSERVER_INFO_1530
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVER_INFO_1530
 - lmserver/_SERVER_INFO_1530
 - PSERVER_INFO_1530
 - lmserver/PSERVER_INFO_1530
 - SERVER_INFO_1530
 - lmserver/SERVER_INFO_1530
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
 - SERVER_INFO_1530
---

# SERVER_INFO_1530 structure


## -description

The
				<b>SERVER_INFO_1530</b> structure specifies the minimum number of available receive work items the server requires to begin processing a server message block.

## -struct-fields

### -field sv1530_minfreeworkitems

Specifies the minimum number of available receive work items that the server requires to begin processing a server message block. A larger value for this member ensures that work items are available more frequently for nonblocking requests, but it also increases the likelihood that blocking requests will be rejected.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/server-functions">Server Functions</a>