---
UID: NS:lmserver._SERVER_INFO_1010
title: "_SERVER_INFO_1010"
author: windows-driver-content
description: The SERVER_INFO_1010 structure contains the auto-disconnect time associated with the specified server.
old-location: netmgmt\server_info_1010_str.htm
old-project: NetMgmt
ms.assetid: 54ae857d-91bb-4f60-b678-07e3b4661ef0
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: "*LPSERVER_INFO_1010, *PSERVER_INFO_1010, LPSERVER_INFO_1010, LPSERVER_INFO_1010 structure pointer [Network Management], PSERVER_INFO_1010, PSERVER_INFO_1010 structure pointer [Network Management], SERVER_INFO_1010, SERVER_INFO_1010 structure [Network Management], _SERVER_INFO_1010, _win32_server_info_1010_str, lmserver/LPSERVER_INFO_1010, lmserver/PSERVER_INFO_1010, lmserver/SERVER_INFO_1010, netmgmt.server_info_1010_str"
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
req.typenames: SERVER_INFO_1010, *PSERVER_INFO_1010, *LPSERVER_INFO_1010
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Lmserver.h
api_name:
-	SERVER_INFO_1010
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _SERVER_INFO_1010 structure


## -description


The
				<b>SERVER_INFO_1010</b> structure contains the auto-disconnect time associated with the specified server.


## -struct-fields




### -field sv1010_disc

Specifies the auto-disconnect time, in minutes. 




If a session is idle longer than the period of time specified by this member, the server disconnects the session. If the value of this member is SV_NODISC, auto-disconnect is not enabled.


## -see-also




<a href="https://msdn.microsoft.com/ed15e1b5-3fdc-4841-85d1-89269684df0e">NetServerGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/43e1285b-8c86-4af4-9834-fcd5ee8aceb8">Server Functions</a>
 

 

