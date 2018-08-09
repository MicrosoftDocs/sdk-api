---
UID: NS:lmserver._SERVER_INFO_1552
title: "_SERVER_INFO_1552"
author: windows-sdk-content
description: The SERVER_INFO_1552 structure specifies the maximum time allowed for a link delay.
old-location: netmgmt\server_info_1552_str.htm
old-project: netmgmt
ms.assetid: eb725f37-4bcd-4402-968f-ea6d58d7d79a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPSERVER_INFO_1552, *PSERVER_INFO_1552, LPSERVER_INFO_1552, LPSERVER_INFO_1552 structure pointer [Network Management], PSERVER_INFO_1552, PSERVER_INFO_1552 structure pointer [Network Management], SERVER_INFO_1552, SERVER_INFO_1552 structure [Network Management], _SERVER_INFO_1552, _win32_server_info_1552_str, lmserver/LPSERVER_INFO_1552, lmserver/PSERVER_INFO_1552, lmserver/SERVER_INFO_1552, netmgmt.server_info_1552_str"
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
tech.root: 
req.typenames: SERVER_INFO_1552, *PSERVER_INFO_1552, *LPSERVER_INFO_1552
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmserver.h
api_name:
 - SERVER_INFO_1552
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _SERVER_INFO_1552 structure


## -description


The
				<b>SERVER_INFO_1552</b> structure specifies the maximum time allowed for a link delay.


## -struct-fields




### -field sv1552_maxlinkdelay

Specifies the maximum time allowed for a link delay, in seconds. If delays exceed this number, the server disables raw I/O for this connection.


## -see-also




<a href="https://msdn.microsoft.com/ed15e1b5-3fdc-4841-85d1-89269684df0e">NetServerGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/43e1285b-8c86-4af4-9834-fcd5ee8aceb8">Server Functions</a>
 

 

