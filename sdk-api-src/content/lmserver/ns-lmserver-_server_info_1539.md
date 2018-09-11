---
UID: NS:lmserver._SERVER_INFO_1539
title: "_SERVER_INFO_1539"
author: windows-sdk-content
description: The SERVER_INFO_1539 structure specifies whether the server processes raw Server Message Blocks (SMBs).
old-location: netmgmt\server_info_1539_str.htm
tech.root: netmgmt
ms.assetid: 938c6db6-16ab-4c8c-8fe3-e12f8e0421b4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPSERVER_INFO_1539, *PSERVER_INFO_1539, LPSERVER_INFO_1539, LPSERVER_INFO_1539 structure pointer [Network Management], PSERVER_INFO_1539, PSERVER_INFO_1539 structure pointer [Network Management], SERVER_INFO_1539, SERVER_INFO_1539 structure [Network Management], _SERVER_INFO_1539, _win32_server_info_1539_str, lmserver/LPSERVER_INFO_1539, lmserver/PSERVER_INFO_1539, lmserver/SERVER_INFO_1539, netmgmt.server_info_1539_str"
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
 - SERVER_INFO_1539
product: Windows
targetos: Windows
req.typenames: SERVER_INFO_1539, *PSERVER_INFO_1539, *LPSERVER_INFO_1539
req.redist: 
---

# _SERVER_INFO_1539 structure


## -description


The
				<b>SERVER_INFO_1539</b> structure specifies whether the server processes raw Server Message Blocks (SMBs).


## -struct-fields




### -field sv1539_enableraw

Specifies whether the server processes raw SMBs. If enabled, this member allows more data to be transferred per transaction and improves performance. However, it is possible that processing raw SMBs can impede performance on certain networks. The server maintains the value of this member.


## -see-also




<a href="https://msdn.microsoft.com/ed15e1b5-3fdc-4841-85d1-89269684df0e">NetServerGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/43e1285b-8c86-4af4-9834-fcd5ee8aceb8">Server Functions</a>
 

 

