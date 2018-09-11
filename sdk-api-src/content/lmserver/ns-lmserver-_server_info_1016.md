---
UID: NS:lmserver._SERVER_INFO_1016
title: "_SERVER_INFO_1016"
author: windows-sdk-content
description: The SERVER_INFO_1016 structure contains information about whether the server is visible to other computers in the same network domain.
old-location: netmgmt\server_info_1016_str.htm
tech.root: netmgmt
ms.assetid: a4c2afaf-05a4-4b71-9b36-91c603cba9d7
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPSERVER_INFO_1016, *PSERVER_INFO_1016, LPSERVER_INFO_1016, LPSERVER_INFO_1016 structure pointer [Network Management], PSERVER_INFO_1016, PSERVER_INFO_1016 structure pointer [Network Management], SERVER_INFO_1016, SERVER_INFO_1016 structure [Network Management], SV_HIDDEN, SV_VISIBLE, _SERVER_INFO_1016, _win32_server_info_1016_str, lmserver/LPSERVER_INFO_1016, lmserver/PSERVER_INFO_1016, lmserver/SERVER_INFO_1016, netmgmt.server_info_1016_str"
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
 - SERVER_INFO_1016
product: Windows
targetos: Windows
req.typenames: SERVER_INFO_1016, *PSERVER_INFO_1016, *LPSERVER_INFO_1016
req.redist: 
---

# _SERVER_INFO_1016 structure


## -description


The
				<b>SERVER_INFO_1016</b> structure contains information about whether the server is visible to other computers in the same network domain.


## -struct-fields




### -field sv1016_hidden

Specifies whether the server is visible to other computers in the same network domain. This member can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SV_VISIBLE"></a><a id="sv_visible"></a><dl>
<dt><b>SV_VISIBLE</b></dt>
</dl>
</td>
<td width="60%">
The server is visible.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_HIDDEN"></a><a id="sv_hidden"></a><dl>
<dt><b>SV_HIDDEN</b></dt>
</dl>
</td>
<td width="60%">
The server is not visible.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/ed15e1b5-3fdc-4841-85d1-89269684df0e">NetServerGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/43e1285b-8c86-4af4-9834-fcd5ee8aceb8">Server Functions</a>
 

 

