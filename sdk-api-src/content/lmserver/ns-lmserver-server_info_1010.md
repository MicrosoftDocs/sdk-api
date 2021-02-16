---
UID: NS:lmserver._SERVER_INFO_1010
title: SERVER_INFO_1010 (lmserver.h)
description: The SERVER_INFO_1010 structure contains the auto-disconnect time associated with the specified server.
helpviewer_keywords: ["*LPSERVER_INFO_1010","*PSERVER_INFO_1010","LPSERVER_INFO_1010","LPSERVER_INFO_1010 structure pointer [Network Management]","PSERVER_INFO_1010","PSERVER_INFO_1010 structure pointer [Network Management]","SERVER_INFO_1010","SERVER_INFO_1010 structure [Network Management]","_win32_server_info_1010_str","lmserver/LPSERVER_INFO_1010","lmserver/PSERVER_INFO_1010","lmserver/SERVER_INFO_1010","netmgmt.server_info_1010_str"]
old-location: netmgmt\server_info_1010_str.htm
tech.root: NetMgmt
ms.assetid: 54ae857d-91bb-4f60-b678-07e3b4661ef0
ms.date: 12/05/2018
ms.keywords: '*LPSERVER_INFO_1010, *PSERVER_INFO_1010, LPSERVER_INFO_1010, LPSERVER_INFO_1010 structure pointer [Network Management], PSERVER_INFO_1010, PSERVER_INFO_1010 structure pointer [Network Management], SERVER_INFO_1010, SERVER_INFO_1010 structure [Network Management], _win32_server_info_1010_str, lmserver/LPSERVER_INFO_1010, lmserver/PSERVER_INFO_1010, lmserver/SERVER_INFO_1010, netmgmt.server_info_1010_str'
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
req.typenames: SERVER_INFO_1010, *PSERVER_INFO_1010, *LPSERVER_INFO_1010
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVER_INFO_1010
 - lmserver/_SERVER_INFO_1010
 - PSERVER_INFO_1010
 - lmserver/PSERVER_INFO_1010
 - SERVER_INFO_1010
 - lmserver/SERVER_INFO_1010
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
 - SERVER_INFO_1010
---

# SERVER_INFO_1010 structure


## -description

The
				<b>SERVER_INFO_1010</b> structure contains the auto-disconnect time associated with the specified server.

## -struct-fields

### -field sv1010_disc

Specifies the auto-disconnect time, in minutes. 




If a session is idle longer than the period of time specified by this member, the server disconnects the session. If the value of this member is SV_NODISC, auto-disconnect is not enabled.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/server-functions">Server Functions</a>