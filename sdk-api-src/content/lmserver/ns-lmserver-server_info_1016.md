---
UID: NS:lmserver._SERVER_INFO_1016
title: SERVER_INFO_1016 (lmserver.h)
description: The SERVER_INFO_1016 structure contains information about whether the server is visible to other computers in the same network domain.
helpviewer_keywords: ["*LPSERVER_INFO_1016","*PSERVER_INFO_1016","LPSERVER_INFO_1016","LPSERVER_INFO_1016 structure pointer [Network Management]","PSERVER_INFO_1016","PSERVER_INFO_1016 structure pointer [Network Management]","SERVER_INFO_1016","SERVER_INFO_1016 structure [Network Management]","SV_HIDDEN","SV_VISIBLE","_win32_server_info_1016_str","lmserver/LPSERVER_INFO_1016","lmserver/PSERVER_INFO_1016","lmserver/SERVER_INFO_1016","netmgmt.server_info_1016_str"]
old-location: netmgmt\server_info_1016_str.htm
tech.root: NetMgmt
ms.assetid: a4c2afaf-05a4-4b71-9b36-91c603cba9d7
ms.date: 12/05/2018
ms.keywords: '*LPSERVER_INFO_1016, *PSERVER_INFO_1016, LPSERVER_INFO_1016, LPSERVER_INFO_1016 structure pointer [Network Management], PSERVER_INFO_1016, PSERVER_INFO_1016 structure pointer [Network Management], SERVER_INFO_1016, SERVER_INFO_1016 structure [Network Management], SV_HIDDEN, SV_VISIBLE, _win32_server_info_1016_str, lmserver/LPSERVER_INFO_1016, lmserver/PSERVER_INFO_1016, lmserver/SERVER_INFO_1016, netmgmt.server_info_1016_str'
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
targetos: Windows
req.typenames: SERVER_INFO_1016, *PSERVER_INFO_1016, *LPSERVER_INFO_1016
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVER_INFO_1016
 - lmserver/_SERVER_INFO_1016
 - PSERVER_INFO_1016
 - lmserver/PSERVER_INFO_1016
 - SERVER_INFO_1016
 - lmserver/SERVER_INFO_1016
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmserver.h
api_name:
 - SERVER_INFO_1016
---

# SERVER_INFO_1016 structure


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

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/server-functions">Server Functions</a>