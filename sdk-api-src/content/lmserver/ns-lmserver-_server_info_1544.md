---
UID: NS:lmserver._SERVER_INFO_1544
title: "_SERVER_INFO_1544"
author: windows-sdk-content
description: The SERVER_INFO_1544 structure specifies the initial number of tree connections to be allocated in the connection table.
old-location: netmgmt\server_info_1544_str.htm
old-project: NetMgmt
ms.assetid: 11a985b0-b092-44f0-83b9-4628a01db00e
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*LPSERVER_INFO_1544, *PSERVER_INFO_1544, LPSERVER_INFO_1544, LPSERVER_INFO_1544 structure pointer [Network Management], PSERVER_INFO_1544, PSERVER_INFO_1544 structure pointer [Network Management], SERVER_INFO_1544, SERVER_INFO_1544 structure [Network Management], _SERVER_INFO_1544, _win32_server_info_1544_str, lmserver/LPSERVER_INFO_1544, lmserver/PSERVER_INFO_1544, lmserver/SERVER_INFO_1544, netmgmt.server_info_1544_str"
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: SERVER_INFO_1544, *PSERVER_INFO_1544, *LPSERVER_INFO_1544
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Lmserver.h
api_name:
-	SERVER_INFO_1544
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _SERVER_INFO_1544 structure


## -description


The
				<b>SERVER_INFO_1544</b> structure specifies the initial number of tree connections to be allocated in the connection table.


## -struct-fields




### -field sv1544_initconntable

Specifies the initial number of tree connections to be allocated in the connection table. The server automatically increases the table as necessary, so setting the member to a higher value is an optimization.


## -see-also




<a href="https://msdn.microsoft.com/ed15e1b5-3fdc-4841-85d1-89269684df0e">NetServerGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/43e1285b-8c86-4af4-9834-fcd5ee8aceb8">Server Functions</a>
 

 

