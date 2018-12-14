---
UID: NS:lmserver._SERVER_INFO_1542
title: SERVER_INFO_1542
author: windows-sdk-content
description: The SERVER_INFO_1542 structure specifies the maximum number of free connection blocks the server sets aside to handle bursts of requests by clients to connect to the server.
old-location: netmgmt\server_info_1542_str.htm
tech.root: netmgmt
ms.assetid: 49c38acd-ed20-4ddc-a97a-9d77b8907378
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPSERVER_INFO_1542, *PSERVER_INFO_1542, LPSERVER_INFO_1542, LPSERVER_INFO_1542 structure pointer [Network Management], PSERVER_INFO_1542, PSERVER_INFO_1542 structure pointer [Network Management], SERVER_INFO_1542, SERVER_INFO_1542 structure [Network Management], _win32_server_info_1542_str, lmserver/LPSERVER_INFO_1542, lmserver/PSERVER_INFO_1542, lmserver/SERVER_INFO_1542, netmgmt.server_info_1542_str"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - SERVER_INFO_1542
product: Windows
targetos: Windows
req.typenames: SERVER_INFO_1542, *PSERVER_INFO_1542, *LPSERVER_INFO_1542
req.redist: 
---

# SERVER_INFO_1542 structure


## -description


The
				<b>SERVER_INFO_1542</b> structure specifies the maximum number of free connection blocks the server sets aside to handle bursts of requests by clients to connect to the server.


## -struct-fields




### -field sv1542_maxfreeconnections

Specifies the maximum number of free connection blocks maintained per endpoint. The server sets these aside to handle bursts of requests by clients to connect to the server.


## -see-also




<a href="https://msdn.microsoft.com/ed15e1b5-3fdc-4841-85d1-89269684df0e">NetServerGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/43e1285b-8c86-4af4-9834-fcd5ee8aceb8">Server Functions</a>
 

 

