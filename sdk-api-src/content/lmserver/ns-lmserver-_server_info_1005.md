---
UID: NS:lmserver._SERVER_INFO_1005
title: "_SERVER_INFO_1005"
author: windows-sdk-content
description: The SERVER_INFO_1005 structure contains a comment that describes the specified server.
old-location: netmgmt\server_info_1005_str.htm
tech.root: netmgmt
ms.assetid: a8ce88ee-2b44-4b12-ba7a-f84249a3621b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPSERVER_INFO_1005, *PSERVER_INFO_1005, LPSERVER_INFO_1005, LPSERVER_INFO_1005 structure pointer [Network Management], PSERVER_INFO_1005, PSERVER_INFO_1005 structure pointer [Network Management], SERVER_INFO_1005, SERVER_INFO_1005 structure [Network Management], _SERVER_INFO_1005, _win32_server_info_1005_str, lmserver/LPSERVER_INFO_1005, lmserver/PSERVER_INFO_1005, lmserver/SERVER_INFO_1005, netmgmt.server_info_1005_str"
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
 - SERVER_INFO_1005
product: Windows
targetos: Windows
req.typenames: SERVER_INFO_1005, *PSERVER_INFO_1005, *LPSERVER_INFO_1005
req.redist: 
---

# _SERVER_INFO_1005 structure


## -description


The
				<b>SERVER_INFO_1005</b> structure contains a comment that describes the specified server.


## -struct-fields




### -field sv1005_comment

Pointer to a string that contains a comment describing the server. The comment can be null.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.


## -see-also




<a href="https://msdn.microsoft.com/ed15e1b5-3fdc-4841-85d1-89269684df0e">NetServerGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/43e1285b-8c86-4af4-9834-fcd5ee8aceb8">Server Functions</a>
 

 

