---
UID: NS:lmserver._SERVER_INFO_1539
title: SERVER_INFO_1539 (lmserver.h)
description: The SERVER_INFO_1539 structure specifies whether the server processes raw Server Message Blocks (SMBs).
helpviewer_keywords: ["*LPSERVER_INFO_1539","*PSERVER_INFO_1539","LPSERVER_INFO_1539","LPSERVER_INFO_1539 structure pointer [Network Management]","PSERVER_INFO_1539","PSERVER_INFO_1539 structure pointer [Network Management]","SERVER_INFO_1539","SERVER_INFO_1539 structure [Network Management]","_win32_server_info_1539_str","lmserver/LPSERVER_INFO_1539","lmserver/PSERVER_INFO_1539","lmserver/SERVER_INFO_1539","netmgmt.server_info_1539_str"]
old-location: netmgmt\server_info_1539_str.htm
tech.root: NetMgmt
ms.assetid: 938c6db6-16ab-4c8c-8fe3-e12f8e0421b4
ms.date: 12/05/2018
ms.keywords: '*LPSERVER_INFO_1539, *PSERVER_INFO_1539, LPSERVER_INFO_1539, LPSERVER_INFO_1539 structure pointer [Network Management], PSERVER_INFO_1539, PSERVER_INFO_1539 structure pointer [Network Management], SERVER_INFO_1539, SERVER_INFO_1539 structure [Network Management], _win32_server_info_1539_str, lmserver/LPSERVER_INFO_1539, lmserver/PSERVER_INFO_1539, lmserver/SERVER_INFO_1539, netmgmt.server_info_1539_str'
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
req.typenames: SERVER_INFO_1539, *PSERVER_INFO_1539, *LPSERVER_INFO_1539
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVER_INFO_1539
 - lmserver/_SERVER_INFO_1539
 - PSERVER_INFO_1539
 - lmserver/PSERVER_INFO_1539
 - SERVER_INFO_1539
 - lmserver/SERVER_INFO_1539
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
 - SERVER_INFO_1539
---

# SERVER_INFO_1539 structure


## -description

The
				<b>SERVER_INFO_1539</b> structure specifies whether the server processes raw Server Message Blocks (SMBs).

## -struct-fields

### -field sv1539_enableraw

Specifies whether the server processes raw SMBs. If enabled, this member allows more data to be transferred per transaction and improves performance. However, it is possible that processing raw SMBs can impede performance on certain networks. The server maintains the value of this member.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/server-functions">Server Functions</a>