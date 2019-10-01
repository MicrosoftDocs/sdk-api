---
UID: NS:lmserver._SERVER_INFO_1533
title: SERVER_INFO_1533 (lmserver.h)
author: windows-sdk-content
description: The SERVER_INFO_1533 structure specifies the maximum number of outstanding requests a client can send to the server.
old-location: netmgmt\server_info_1533_str.htm
tech.root: NetMgmt
ms.assetid: 2b54dcec-c456-4cef-a2b9-eb24adf4a994
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPSERVER_INFO_1533, *PSERVER_INFO_1533, LPSERVER_INFO_1533, LPSERVER_INFO_1533 structure pointer [Network Management], PSERVER_INFO_1533, PSERVER_INFO_1533 structure pointer [Network Management], SERVER_INFO_1533, SERVER_INFO_1533 structure [Network Management], _win32_server_info_1533_str, lmserver/LPSERVER_INFO_1533, lmserver/PSERVER_INFO_1533, lmserver/SERVER_INFO_1533, netmgmt.server_info_1533_str"
ms.topic: struct
f1_keywords: 
 - "lmserver/SERVER_INFO_1533"
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
targetos: Windows
req.typenames: SERVER_INFO_1533, *PSERVER_INFO_1533, *LPSERVER_INFO_1533
req.redist: 
ms.custom: 19H1
---

# SERVER_INFO_1533 structure


## -description


The
				<b>SERVER_INFO_1533</b> structure specifies the maximum number of outstanding requests a client can send to the server.


## -struct-fields




### -field sv1533_maxmpxct

Specifies the maximum number of outstanding requests any one client can send to the server. For example, 10 means you can have 10 unanswered requests at the server. When any single client has 10 requests queued within the server, the client must wait for a server response before sending another request.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/server-functions">Server Functions</a>
 

 

