---
UID: NS:lmserver._SERVER_INFO_1005
title: SERVER_INFO_1005 (lmserver.h)
author: windows-sdk-content
description: The SERVER_INFO_1005 structure contains a comment that describes the specified server.
old-location: netmgmt\server_info_1005_str.htm
tech.root: NetMgmt
ms.assetid: a8ce88ee-2b44-4b12-ba7a-f84249a3621b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPSERVER_INFO_1005, *PSERVER_INFO_1005, LPSERVER_INFO_1005, LPSERVER_INFO_1005 structure pointer [Network Management], PSERVER_INFO_1005, PSERVER_INFO_1005 structure pointer [Network Management], SERVER_INFO_1005, SERVER_INFO_1005 structure [Network Management], _win32_server_info_1005_str, lmserver/LPSERVER_INFO_1005, lmserver/PSERVER_INFO_1005, lmserver/SERVER_INFO_1005, netmgmt.server_info_1005_str"
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
ms.custom: 19H1
---

# SERVER_INFO_1005 structure


## -description


The
				<b>SERVER_INFO_1005</b> structure contains a comment that describes the specified server.


## -struct-fields




### -field sv1005_comment

Pointer to a string that contains a comment describing the server. The comment can be null.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/server-functions">Server Functions</a>
 

 

