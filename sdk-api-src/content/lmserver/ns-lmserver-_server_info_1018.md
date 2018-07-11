---
UID: NS:lmserver._SERVER_INFO_1018
title: "_SERVER_INFO_1018"
author: windows-sdk-content
description: The SERVER_INFO_1018 structure contains information about how much the announce rate can vary for the specified server.
old-location: netmgmt\server_info_1018_str.htm
old-project: netmgmt
ms.assetid: 0a87d88c-af70-41ce-9d92-6e642d284819
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: "*LPSERVER_INFO_1018, *PSERVER_INFO_1018, LPSERVER_INFO_1018, LPSERVER_INFO_1018 structure pointer [Network Management], PSERVER_INFO_1018, PSERVER_INFO_1018 structure pointer [Network Management], SERVER_INFO_1018, SERVER_INFO_1018 structure [Network Management], _SERVER_INFO_1018, _win32_server_info_1018_str, lmserver/LPSERVER_INFO_1018, lmserver/PSERVER_INFO_1018, lmserver/SERVER_INFO_1018, netmgmt.server_info_1018_str"
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
req.typenames: SERVER_INFO_1018, *PSERVER_INFO_1018, *LPSERVER_INFO_1018
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmserver.h
api_name:
 - SERVER_INFO_1018
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _SERVER_INFO_1018 structure


## -description


The
				<b>SERVER_INFO_1018</b> structure contains information about how much the announce rate can vary for the specified server.


## -struct-fields




### -field sv1018_anndelta

Specifies the delta value for the announce rate, in milliseconds. This value specifies how much the announce rate can vary from the period of time specified in the sv<i>X</i>_announce member. 




The delta value allows randomly varied announce rates. For example, if the sv<i>X</i>_announce member has the value 10 and the sv<i>X</i>_anndelta member has the value 1, the announce rate can vary from 9.999 seconds to 10.001 seconds. For more information, see 
<a href="https://msdn.microsoft.com/4c63fee7-1103-414d-b650-da87f8184e91">SERVER_INFO_102</a> and 
<a href="https://msdn.microsoft.com/ad169dd2-6469-499d-b6be-53d99a92148f">SERVER_INFO_1017</a>.


## -see-also




<a href="https://msdn.microsoft.com/ed15e1b5-3fdc-4841-85d1-89269684df0e">NetServerGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/ad169dd2-6469-499d-b6be-53d99a92148f">SERVER_INFO_1017</a>



<a href="https://msdn.microsoft.com/4c63fee7-1103-414d-b650-da87f8184e91">SERVER_INFO_102</a>



<a href="https://msdn.microsoft.com/43e1285b-8c86-4af4-9834-fcd5ee8aceb8">Server Functions</a>
 

 

