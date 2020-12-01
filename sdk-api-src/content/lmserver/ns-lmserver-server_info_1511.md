---
UID: NS:lmserver._SERVER_INFO_1511
title: SERVER_INFO_1511 (lmserver.h)
description: The SERVER_INFO_1511 structure specifies the maximum number of tree connections that users can make with a single virtual circuit.
helpviewer_keywords: ["*LPSERVER_INFO_1511","*PSERVER_INFO_1511","LPSERVER_INFO_1511","LPSERVER_INFO_1511 structure pointer [Network Management]","PSERVER_INFO_1511","PSERVER_INFO_1511 structure pointer [Network Management]","SERVER_INFO_1511","SERVER_INFO_1511 structure [Network Management]","_win32_server_info_1511_str","lmserver/LPSERVER_INFO_1511","lmserver/PSERVER_INFO_1511","lmserver/SERVER_INFO_1511","netmgmt.server_info_1511_str"]
old-location: netmgmt\server_info_1511_str.htm
tech.root: NetMgmt
ms.assetid: 07865b85-5d08-46ab-9cce-6eba2e14d1b6
ms.date: 12/05/2018
ms.keywords: '*LPSERVER_INFO_1511, *PSERVER_INFO_1511, LPSERVER_INFO_1511, LPSERVER_INFO_1511 structure pointer [Network Management], PSERVER_INFO_1511, PSERVER_INFO_1511 structure pointer [Network Management], SERVER_INFO_1511, SERVER_INFO_1511 structure [Network Management], _win32_server_info_1511_str, lmserver/LPSERVER_INFO_1511, lmserver/PSERVER_INFO_1511, lmserver/SERVER_INFO_1511, netmgmt.server_info_1511_str'
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
req.typenames: SERVER_INFO_1511, *PSERVER_INFO_1511, *LPSERVER_INFO_1511
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVER_INFO_1511
 - lmserver/_SERVER_INFO_1511
 - PSERVER_INFO_1511
 - lmserver/PSERVER_INFO_1511
 - SERVER_INFO_1511
 - lmserver/SERVER_INFO_1511
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
 - SERVER_INFO_1511
---

# SERVER_INFO_1511 structure


## -description

The
				<b>SERVER_INFO_1511</b> structure specifies the maximum number of tree connections that users can make with a single virtual circuit.

## -struct-fields

### -field sv1511_sessconns

Specifies the maximum number of tree connections that users can make with a single virtual circuit.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/server-functions">Server Functions</a>