---
UID: NS:lmserver._SERVER_INFO_1529
title: SERVER_INFO_1529 (lmserver.h)
description: The SERVER_INFO_1529 structure specifies the minimum number of free receive work items the server requires before it begins allocating more items.
helpviewer_keywords: ["*LPSERVER_INFO_1529","*PSERVER_INFO_1529","LPSERVER_INFO_1529","LPSERVER_INFO_1529 structure pointer [Network Management]","PSERVER_INFO_1529","PSERVER_INFO_1529 structure pointer [Network Management]","SERVER_INFO_1529","SERVER_INFO_1529 structure [Network Management]","_win32_server_info_1529_str","lmserver/LPSERVER_INFO_1529","lmserver/PSERVER_INFO_1529","lmserver/SERVER_INFO_1529","netmgmt.server_info_1529_str"]
old-location: netmgmt\server_info_1529_str.htm
tech.root: NetMgmt
ms.assetid: 575cb0fa-b011-42a9-9344-02088effeb9b
ms.date: 12/05/2018
ms.keywords: '*LPSERVER_INFO_1529, *PSERVER_INFO_1529, LPSERVER_INFO_1529, LPSERVER_INFO_1529 structure pointer [Network Management], PSERVER_INFO_1529, PSERVER_INFO_1529 structure pointer [Network Management], SERVER_INFO_1529, SERVER_INFO_1529 structure [Network Management], _win32_server_info_1529_str, lmserver/LPSERVER_INFO_1529, lmserver/PSERVER_INFO_1529, lmserver/SERVER_INFO_1529, netmgmt.server_info_1529_str'
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
req.typenames: SERVER_INFO_1529, *PSERVER_INFO_1529, *LPSERVER_INFO_1529
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVER_INFO_1529
 - lmserver/_SERVER_INFO_1529
 - PSERVER_INFO_1529
 - lmserver/PSERVER_INFO_1529
 - SERVER_INFO_1529
 - lmserver/SERVER_INFO_1529
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
 - SERVER_INFO_1529
---

# SERVER_INFO_1529 structure


## -description

The
				<b>SERVER_INFO_1529</b> structure specifies the minimum number of free receive work items the server requires before it begins allocating more items.

## -struct-fields

### -field sv1529_minrcvqueue

Specifies the minimum number of free receive work items the server requires before it begins allocating more. A larger value for this member helps ensure that there will always be work items available, but a value that is too large is inefficient.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/server-functions">Server Functions</a>