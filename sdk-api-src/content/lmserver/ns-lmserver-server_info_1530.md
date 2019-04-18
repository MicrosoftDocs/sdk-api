---
UID: NS:lmserver._SERVER_INFO_1530
title: SERVER_INFO_1530 (lmserver.h)
author: windows-sdk-content
description: The SERVER_INFO_1530 structure specifies the minimum number of available receive work items the server requires to begin processing a server message block.
old-location: netmgmt\server_info_1530_str.htm
tech.root: NetMgmt
ms.assetid: 972c69e6-9f9c-49c2-a799-7b72dd8aa696
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPSERVER_INFO_1530, *PSERVER_INFO_1530, LPSERVER_INFO_1530, LPSERVER_INFO_1530 structure pointer [Network Management], PSERVER_INFO_1530, PSERVER_INFO_1530 structure pointer [Network Management], SERVER_INFO_1530, SERVER_INFO_1530 structure [Network Management], _win32_server_info_1530_str, lmserver/LPSERVER_INFO_1530, lmserver/PSERVER_INFO_1530, lmserver/SERVER_INFO_1530, netmgmt.server_info_1530_str"
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
 - SERVER_INFO_1530
product: Windows
targetos: Windows
req.typenames: SERVER_INFO_1530, *PSERVER_INFO_1530, *LPSERVER_INFO_1530
req.redist: 
ms.custom: 19H1
---

# SERVER_INFO_1530 structure


## -description


The
				<b>SERVER_INFO_1530</b> structure specifies the minimum number of available receive work items the server requires to begin processing a server message block.


## -struct-fields




### -field sv1530_minfreeworkitems

Specifies the minimum number of available receive work items that the server requires to begin processing a server message block. A larger value for this member ensures that work items are available more frequently for nonblocking requests, but it also increases the likelihood that blocking requests will be rejected.


## -see-also




<a href="https://msdn.microsoft.com/ed15e1b5-3fdc-4841-85d1-89269684df0e">NetServerGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/43e1285b-8c86-4af4-9834-fcd5ee8aceb8">Server Functions</a>
 

 

