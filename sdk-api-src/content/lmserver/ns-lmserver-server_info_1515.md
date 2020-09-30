---
UID: NS:lmserver._SERVER_INFO_1515
title: SERVER_INFO_1515 (lmserver.h)
description: The SERVER_INFO_1515 structure specifies whether the server should force a client to disconnect once the client's logon time has expired.
helpviewer_keywords: ["*LPSERVER_INFO_1515","*PSERVER_INFO_1515","LPSERVER_INFO_1515","LPSERVER_INFO_1515 structure pointer [Network Management]","PSERVER_INFO_1515","PSERVER_INFO_1515 structure pointer [Network Management]","SERVER_INFO_1515","SERVER_INFO_1515 structure [Network Management]","_win32_server_info_1515_str","lmserver/LPSERVER_INFO_1515","lmserver/PSERVER_INFO_1515","lmserver/SERVER_INFO_1515","netmgmt.server_info_1515_str"]
old-location: netmgmt\server_info_1515_str.htm
tech.root: NetMgmt
ms.assetid: f9aa8580-47c6-4e3e-9e34-dc90cd5178ce
ms.date: 12/05/2018
ms.keywords: '*LPSERVER_INFO_1515, *PSERVER_INFO_1515, LPSERVER_INFO_1515, LPSERVER_INFO_1515 structure pointer [Network Management], PSERVER_INFO_1515, PSERVER_INFO_1515 structure pointer [Network Management], SERVER_INFO_1515, SERVER_INFO_1515 structure [Network Management], _win32_server_info_1515_str, lmserver/LPSERVER_INFO_1515, lmserver/PSERVER_INFO_1515, lmserver/SERVER_INFO_1515, netmgmt.server_info_1515_str'
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
req.typenames: SERVER_INFO_1515, *PSERVER_INFO_1515, *LPSERVER_INFO_1515
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVER_INFO_1515
 - lmserver/_SERVER_INFO_1515
 - PSERVER_INFO_1515
 - lmserver/PSERVER_INFO_1515
 - SERVER_INFO_1515
 - lmserver/SERVER_INFO_1515
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
 - SERVER_INFO_1515
---

# SERVER_INFO_1515 structure


## -description

The
				<b>SERVER_INFO_1515</b> structure specifies whether the server should force a client to disconnect once the client's logon time has expired.

## -struct-fields

### -field sv1515_enableforcedlogoff

Specifies whether the server should force a client to disconnect, even if the client has open files, once the client's logon time has expired.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/server-functions">Server Functions</a>