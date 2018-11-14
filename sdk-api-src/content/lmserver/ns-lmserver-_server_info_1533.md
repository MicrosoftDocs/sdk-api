---
UID: NS:lmserver._SERVER_INFO_1533
title: "_SERVER_INFO_1533"
author: windows-sdk-content
description: The SERVER_INFO_1533 structure specifies the maximum number of outstanding requests a client can send to the server.
old-location: netmgmt\server_info_1533_str.htm
tech.root: NetMgmt
ms.assetid: 2b54dcec-c456-4cef-a2b9-eb24adf4a994
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPSERVER_INFO_1533, *PSERVER_INFO_1533, LPSERVER_INFO_1533, LPSERVER_INFO_1533 structure pointer [Network Management], PSERVER_INFO_1533, PSERVER_INFO_1533 structure pointer [Network Management], SERVER_INFO_1533, SERVER_INFO_1533 structure [Network Management], _SERVER_INFO_1533, _win32_server_info_1533_str, lmserver/LPSERVER_INFO_1533, lmserver/PSERVER_INFO_1533, lmserver/SERVER_INFO_1533, netmgmt.server_info_1533_str"
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
 - SERVER_INFO_1533
product: Windows
targetos: Windows
req.typenames: SERVER_INFO_1533, *PSERVER_INFO_1533, *LPSERVER_INFO_1533
req.redist: 
---

# _SERVER_INFO_1533 structure


## -description


The
				<b>SERVER_INFO_1533</b> structure specifies the maximum number of outstanding requests a client can send to the server.


## -struct-fields




### -field sv1533_maxmpxct

Specifies the maximum number of outstanding requests any one client can send to the server. For example, 10 means you can have 10 unanswered requests at the server. When any single client has 10 requests queued within the server, the client must wait for a server response before sending another request.


## -see-also




<a href="https://msdn.microsoft.com/ed15e1b5-3fdc-4841-85d1-89269684df0e">NetServerGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/43e1285b-8c86-4af4-9834-fcd5ee8aceb8">Server Functions</a>
 

 

