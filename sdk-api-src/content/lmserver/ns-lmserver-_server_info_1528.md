---
UID: NS:lmserver._SERVER_INFO_1528
title: "_SERVER_INFO_1528"
author: windows-driver-content
description: The SERVER_INFO_1528 structure specifies the period of time that the scavenger remains idle before waking up to service requests.
old-location: netmgmt\server_info_1528_str.htm
old-project: NetMgmt
ms.assetid: 59f7f52b-2bf4-49b0-8e45-472ba290acee
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: "*LPSERVER_INFO_1528, *PSERVER_INFO_1528, LPSERVER_INFO_1528, LPSERVER_INFO_1528 structure pointer [Network Management], PSERVER_INFO_1528, PSERVER_INFO_1528 structure pointer [Network Management], SERVER_INFO_1528, SERVER_INFO_1528 structure [Network Management], _SERVER_INFO_1528, _win32_server_info_1528_str, lmserver/LPSERVER_INFO_1528, lmserver/PSERVER_INFO_1528, lmserver/SERVER_INFO_1528, netmgmt.server_info_1528_str"
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
req.typenames: SERVER_INFO_1528, *PSERVER_INFO_1528, *LPSERVER_INFO_1528
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Lmserver.h
api_name:
-	SERVER_INFO_1528
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _SERVER_INFO_1528 structure


## -description


The
				<b>SERVER_INFO_1528</b> structure specifies the period of time that the scavenger remains idle before waking up to service requests.


## -struct-fields




### -field sv1528_scavtimeout

Specifies the period of time, in seconds, that the scavenger remains idle before waking up to service requests. A smaller value for this member improves the response of the server to various events but costs CPU cycles.


## -see-also




<a href="https://msdn.microsoft.com/ed15e1b5-3fdc-4841-85d1-89269684df0e">NetServerGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/43e1285b-8c86-4af4-9834-fcd5ee8aceb8">Server Functions</a>
 

 

