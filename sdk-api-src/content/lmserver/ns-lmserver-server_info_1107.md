---
UID: NS:lmserver._SERVER_INFO_1107
title: SERVER_INFO_1107 (lmserver.h)
author: windows-sdk-content
description: The SERVER_INFO_1107 structure specifies the number of users that can simultaneously log on to the specified server.
old-location: netmgmt\server_info_1107_str.htm
tech.root: NetMgmt
ms.assetid: 8e0b9157-5f06-4555-ab9e-b98b99e0f20d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPSERVER_INFO_1107, *PSERVER_INFO_1107, LPSERVER_INFO_1107, LPSERVER_INFO_1107 structure pointer [Network Management], PSERVER_INFO_1107, PSERVER_INFO_1107 structure pointer [Network Management], SERVER_INFO_1107, SERVER_INFO_1107 structure [Network Management], _win32_server_info_1107_str, lmserver/LPSERVER_INFO_1107, lmserver/PSERVER_INFO_1107, lmserver/SERVER_INFO_1107, netmgmt.server_info_1107_str"
ms.topic: struct
f1_keywords: 
 - "lmserver/SERVER_INFO_1107"
dev_langs:
 - c++
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
 - SERVER_INFO_1107
targetos: Windows
req.typenames: SERVER_INFO_1107, *PSERVER_INFO_1107, *LPSERVER_INFO_1107
req.redist: 
ms.custom: 19H1
---

# SERVER_INFO_1107 structure


## -description


The
				<b>SERVER_INFO_1107</b> structure specifies the number of users that can simultaneously log on to the specified server.


## -struct-fields




### -field sv1107_users

Specifies the number of users who can attempt to log on to the system server. Note that it is the license server that determines how many of these users can actually log on.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/server-functions">Server Functions</a>
 

 

