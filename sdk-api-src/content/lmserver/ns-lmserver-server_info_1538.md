---
UID: NS:lmserver._SERVER_INFO_1538
title: SERVER_INFO_1538 (lmserver.h)
description: The SERVER_INFO_1538 structure specifies whether several MS-DOS File Control Blocks (FCBs) are placed in a single location.
helpviewer_keywords: ["*LPSERVER_INFO_1538","*PSERVER_INFO_1538","LPSERVER_INFO_1538","LPSERVER_INFO_1538 structure pointer [Network Management]","PSERVER_INFO_1538","PSERVER_INFO_1538 structure pointer [Network Management]","SERVER_INFO_1538","SERVER_INFO_1538 structure [Network Management]","_win32_server_info_1538_str","lmserver/LPSERVER_INFO_1538","lmserver/PSERVER_INFO_1538","lmserver/SERVER_INFO_1538","netmgmt.server_info_1538_str"]
old-location: netmgmt\server_info_1538_str.htm
tech.root: NetMgmt
ms.assetid: 4e11d2f5-27e5-480d-8486-d683bea22781
ms.date: 12/05/2018
ms.keywords: '*LPSERVER_INFO_1538, *PSERVER_INFO_1538, LPSERVER_INFO_1538, LPSERVER_INFO_1538 structure pointer [Network Management], PSERVER_INFO_1538, PSERVER_INFO_1538 structure pointer [Network Management], SERVER_INFO_1538, SERVER_INFO_1538 structure [Network Management], _win32_server_info_1538_str, lmserver/LPSERVER_INFO_1538, lmserver/PSERVER_INFO_1538, lmserver/SERVER_INFO_1538, netmgmt.server_info_1538_str'
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
req.typenames: SERVER_INFO_1538, *PSERVER_INFO_1538, *LPSERVER_INFO_1538
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVER_INFO_1538
 - lmserver/_SERVER_INFO_1538
 - PSERVER_INFO_1538
 - lmserver/PSERVER_INFO_1538
 - SERVER_INFO_1538
 - lmserver/SERVER_INFO_1538
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
 - SERVER_INFO_1538
---

# SERVER_INFO_1538 structure


## -description

The
				<b>SERVER_INFO_1538</b> structure specifies whether several MS-DOS File Control Blocks (FCBs) are placed in a single location.

## -struct-fields

### -field sv1538_enablefcbopens

Specifies whether several MS-DOS File Control Blocks (FCBs) are placed in a single location accessible to the server.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/server-functions">Server Functions</a>