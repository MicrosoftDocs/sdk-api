---
UID: NS:lmserver._SERVER_INFO_1501
title: SERVER_INFO_1501 (lmserver.h)
description: The SERVER_INFO_1501 structure specifies the number of files that can be open in one session on the specified server.
helpviewer_keywords: ["*LPSERVER_INFO_1501","*PSERVER_INFO_1501","LPSERVER_INFO_1501","LPSERVER_INFO_1501 structure pointer [Network Management]","PSERVER_INFO_1501","PSERVER_INFO_1501 structure pointer [Network Management]","SERVER_INFO_1501","SERVER_INFO_1501 structure [Network Management]","_win32_server_info_1501_str","lmserver/LPSERVER_INFO_1501","lmserver/PSERVER_INFO_1501","lmserver/SERVER_INFO_1501","netmgmt.server_info_1501_str"]
old-location: netmgmt\server_info_1501_str.htm
tech.root: NetMgmt
ms.assetid: ed0325ed-1e4b-465b-931c-ff3a4bb3b103
ms.date: 12/05/2018
ms.keywords: '*LPSERVER_INFO_1501, *PSERVER_INFO_1501, LPSERVER_INFO_1501, LPSERVER_INFO_1501 structure pointer [Network Management], PSERVER_INFO_1501, PSERVER_INFO_1501 structure pointer [Network Management], SERVER_INFO_1501, SERVER_INFO_1501 structure [Network Management], _win32_server_info_1501_str, lmserver/LPSERVER_INFO_1501, lmserver/PSERVER_INFO_1501, lmserver/SERVER_INFO_1501, netmgmt.server_info_1501_str'
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
req.typenames: SERVER_INFO_1501, *PSERVER_INFO_1501, *LPSERVER_INFO_1501
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVER_INFO_1501
 - lmserver/_SERVER_INFO_1501
 - PSERVER_INFO_1501
 - lmserver/PSERVER_INFO_1501
 - SERVER_INFO_1501
 - lmserver/SERVER_INFO_1501
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
 - SERVER_INFO_1501
---

# SERVER_INFO_1501 structure


## -description

The
				<b>SERVER_INFO_1501</b> structure specifies the number of files that can be open in one session on the specified server.

## -struct-fields

### -field sv1501_sessopens

Specifies the number of files that one session can open.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/server-functions">Server Functions</a>