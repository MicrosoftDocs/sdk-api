---
UID: NS:lmserver._SERVER_INFO_1536
title: SERVER_INFO_1536
author: windows-sdk-content
description: The SERVER_INFO_1536 structure specifies whether the server allows clients to use opportunistic locks (oplocks) on files.
old-location: netmgmt\server_info_1536_str.htm
tech.root: netmgmt
ms.assetid: f16db9b3-c425-4c1e-8491-b2d7e5203420
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPSERVER_INFO_1536, *PSERVER_INFO_1536, LPSERVER_INFO_1536, LPSERVER_INFO_1536 structure pointer [Network Management], PSERVER_INFO_1536, PSERVER_INFO_1536 structure pointer [Network Management], SERVER_INFO_1536, SERVER_INFO_1536 structure [Network Management], _win32_server_info_1536_str, lmserver/LPSERVER_INFO_1536, lmserver/PSERVER_INFO_1536, lmserver/SERVER_INFO_1536, netmgmt.server_info_1536_str"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmserver.h
api_name:
 - SERVER_INFO_1536
product: Windows
targetos: Windows
req.typenames: SERVER_INFO_1536, *PSERVER_INFO_1536, *LPSERVER_INFO_1536
req.redist: 
---

# SERVER_INFO_1536 structure


## -description


The
				<b>SERVER_INFO_1536</b> structure specifies whether the server allows clients to use opportunistic locks (oplocks) on files.


## -struct-fields




### -field sv1536_enableoplocks

Specifies whether the server allows clients to use oplocks on files. Opportunistic locks are a significant performance enhancement, but have the potential to cause lost cached data on some networks, particularly wide-area networks.


## -see-also




<a href="https://msdn.microsoft.com/ed15e1b5-3fdc-4841-85d1-89269684df0e">NetServerGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/43e1285b-8c86-4af4-9834-fcd5ee8aceb8">Server Functions</a>
 

 

