---
UID: NS:lmserver._SERVER_INFO_1017
title: "_SERVER_INFO_1017"
author: windows-driver-content
description: The SERVER_INFO_1017 structure contains the network announce rate associated with the specified server.
old-location: netmgmt\server_info_1017_str.htm
old-project: NetMgmt
ms.assetid: ad169dd2-6469-499d-b6be-53d99a92148f
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: "*LPSERVER_INFO_1017, *PSERVER_INFO_1017, LPSERVER_INFO_1017, LPSERVER_INFO_1017 structure pointer [Network Management], PSERVER_INFO_1017, PSERVER_INFO_1017 structure pointer [Network Management], SERVER_INFO_1017, SERVER_INFO_1017 structure [Network Management], _SERVER_INFO_1017, _win32_server_info_1017_str, lmserver/LPSERVER_INFO_1017, lmserver/PSERVER_INFO_1017, lmserver/SERVER_INFO_1017, netmgmt.server_info_1017_str"
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
req.typenames: SERVER_INFO_1017, *PSERVER_INFO_1017, *LPSERVER_INFO_1017
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Lmserver.h
api_name:
-	SERVER_INFO_1017
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _SERVER_INFO_1017 structure


## -description


The
				<b>SERVER_INFO_1017</b> structure contains the network announce rate associated with the specified server.


## -struct-fields




### -field sv1017_announce

Specifies the network announce rate, in seconds. This rate determines how often the server is announced to other computers on the network. 




For more information about how much the announce rate can vary from the period of time specified by this member, see 
<a href="https://msdn.microsoft.com/0a87d88c-af70-41ce-9d92-6e642d284819">SERVER_INFO_1018</a>.


## -see-also




<a href="https://msdn.microsoft.com/ed15e1b5-3fdc-4841-85d1-89269684df0e">NetServerGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/0a87d88c-af70-41ce-9d92-6e642d284819">SERVER_INFO_1018</a>



<a href="https://msdn.microsoft.com/43e1285b-8c86-4af4-9834-fcd5ee8aceb8">Server Functions</a>
 

 

