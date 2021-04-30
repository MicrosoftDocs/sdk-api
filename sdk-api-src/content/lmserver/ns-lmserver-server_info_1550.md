---
UID: NS:lmserver._SERVER_INFO_1550
title: SERVER_INFO_1550 (lmserver.h)
description: The SERVER_INFO_1550 structure specifies the percentage of free disk space remaining before an alert message is sent.
helpviewer_keywords: ["*LPSERVER_INFO_1550","*PSERVER_INFO_1550","LPSERVER_INFO_1550","LPSERVER_INFO_1550 structure pointer [Network Management]","PSERVER_INFO_1550","PSERVER_INFO_1550 structure pointer [Network Management]","SERVER_INFO_1550","SERVER_INFO_1550 structure [Network Management]","_win32_server_info_1550_str","lmserver/LPSERVER_INFO_1550","lmserver/PSERVER_INFO_1550","lmserver/SERVER_INFO_1550","netmgmt.server_info_1550_str"]
old-location: netmgmt\server_info_1550_str.htm
tech.root: NetMgmt
ms.assetid: 1f352eca-c4dd-4cac-8640-5ff61195be66
ms.date: 12/05/2018
ms.keywords: '*LPSERVER_INFO_1550, *PSERVER_INFO_1550, LPSERVER_INFO_1550, LPSERVER_INFO_1550 structure pointer [Network Management], PSERVER_INFO_1550, PSERVER_INFO_1550 structure pointer [Network Management], SERVER_INFO_1550, SERVER_INFO_1550 structure [Network Management], _win32_server_info_1550_str, lmserver/LPSERVER_INFO_1550, lmserver/PSERVER_INFO_1550, lmserver/SERVER_INFO_1550, netmgmt.server_info_1550_str'
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
req.typenames: SERVER_INFO_1550, *PSERVER_INFO_1550, *LPSERVER_INFO_1550
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVER_INFO_1550
 - lmserver/_SERVER_INFO_1550
 - PSERVER_INFO_1550
 - lmserver/PSERVER_INFO_1550
 - SERVER_INFO_1550
 - lmserver/SERVER_INFO_1550
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
 - SERVER_INFO_1550
---

# SERVER_INFO_1550 structure


## -description

The
				<b>SERVER_INFO_1550</b> structure specifies the percentage of free disk space remaining before an alert message is sent.

## -struct-fields

### -field sv1550_diskspacethreshold

Specifies the percentage of free disk space remaining before an alert message is sent.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/server-functions">Server Functions</a>