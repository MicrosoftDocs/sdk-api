---
UID: NS:lmserver._SERVER_INFO_1528
title: SERVER_INFO_1528 (lmserver.h)
description: The SERVER_INFO_1528 structure specifies the period of time that the scavenger remains idle before waking up to service requests.
helpviewer_keywords: ["*LPSERVER_INFO_1528","*PSERVER_INFO_1528","LPSERVER_INFO_1528","LPSERVER_INFO_1528 structure pointer [Network Management]","PSERVER_INFO_1528","PSERVER_INFO_1528 structure pointer [Network Management]","SERVER_INFO_1528","SERVER_INFO_1528 structure [Network Management]","_win32_server_info_1528_str","lmserver/LPSERVER_INFO_1528","lmserver/PSERVER_INFO_1528","lmserver/SERVER_INFO_1528","netmgmt.server_info_1528_str"]
old-location: netmgmt\server_info_1528_str.htm
tech.root: NetMgmt
ms.assetid: 59f7f52b-2bf4-49b0-8e45-472ba290acee
ms.date: 12/05/2018
ms.keywords: '*LPSERVER_INFO_1528, *PSERVER_INFO_1528, LPSERVER_INFO_1528, LPSERVER_INFO_1528 structure pointer [Network Management], PSERVER_INFO_1528, PSERVER_INFO_1528 structure pointer [Network Management], SERVER_INFO_1528, SERVER_INFO_1528 structure [Network Management], _win32_server_info_1528_str, lmserver/LPSERVER_INFO_1528, lmserver/PSERVER_INFO_1528, lmserver/SERVER_INFO_1528, netmgmt.server_info_1528_str'
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
req.typenames: SERVER_INFO_1528, *PSERVER_INFO_1528, *LPSERVER_INFO_1528
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVER_INFO_1528
 - lmserver/_SERVER_INFO_1528
 - PSERVER_INFO_1528
 - lmserver/PSERVER_INFO_1528
 - SERVER_INFO_1528
 - lmserver/SERVER_INFO_1528
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
 - SERVER_INFO_1528
---

# SERVER_INFO_1528 structure


## -description

The
				<b>SERVER_INFO_1528</b> structure specifies the period of time that the scavenger remains idle before waking up to service requests.

## -struct-fields

### -field sv1528_scavtimeout

Specifies the period of time, in seconds, that the scavenger remains idle before waking up to service requests. A smaller value for this member improves the response of the server to various events but costs CPU cycles.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/server-functions">Server Functions</a>