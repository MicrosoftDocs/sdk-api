---
UID: NS:lmserver._SERVER_INFO_1018
title: SERVER_INFO_1018 (lmserver.h)
description: The SERVER_INFO_1018 structure contains information about how much the announce rate can vary for the specified server.
helpviewer_keywords: ["*LPSERVER_INFO_1018","*PSERVER_INFO_1018","LPSERVER_INFO_1018","LPSERVER_INFO_1018 structure pointer [Network Management]","PSERVER_INFO_1018","PSERVER_INFO_1018 structure pointer [Network Management]","SERVER_INFO_1018","SERVER_INFO_1018 structure [Network Management]","_win32_server_info_1018_str","lmserver/LPSERVER_INFO_1018","lmserver/PSERVER_INFO_1018","lmserver/SERVER_INFO_1018","netmgmt.server_info_1018_str"]
old-location: netmgmt\server_info_1018_str.htm
tech.root: NetMgmt
ms.assetid: 0a87d88c-af70-41ce-9d92-6e642d284819
ms.date: 12/05/2018
ms.keywords: '*LPSERVER_INFO_1018, *PSERVER_INFO_1018, LPSERVER_INFO_1018, LPSERVER_INFO_1018 structure pointer [Network Management], PSERVER_INFO_1018, PSERVER_INFO_1018 structure pointer [Network Management], SERVER_INFO_1018, SERVER_INFO_1018 structure [Network Management], _win32_server_info_1018_str, lmserver/LPSERVER_INFO_1018, lmserver/PSERVER_INFO_1018, lmserver/SERVER_INFO_1018, netmgmt.server_info_1018_str'
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
req.typenames: SERVER_INFO_1018, *PSERVER_INFO_1018, *LPSERVER_INFO_1018
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVER_INFO_1018
 - lmserver/_SERVER_INFO_1018
 - PSERVER_INFO_1018
 - lmserver/PSERVER_INFO_1018
 - SERVER_INFO_1018
 - lmserver/SERVER_INFO_1018
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
 - SERVER_INFO_1018
---

# SERVER_INFO_1018 structure


## -description

The
				<b>SERVER_INFO_1018</b> structure contains information about how much the announce rate can vary for the specified server.

## -struct-fields

### -field sv1018_anndelta

Specifies the delta value for the announce rate, in milliseconds. This value specifies how much the announce rate can vary from the period of time specified in the sv<i>X</i>_announce member. 




The delta value allows randomly varied announce rates. For example, if the sv<i>X</i>_announce member has the value 10 and the sv<i>X</i>_anndelta member has the value 1, the announce rate can vary from 9.999 seconds to 10.001 seconds. For more information, see 
<a href="/windows/desktop/api/lmserver/ns-lmserver-server_info_102">SERVER_INFO_102</a> and 
<a href="/windows/desktop/api/lmserver/ns-lmserver-server_info_1017">SERVER_INFO_1017</a>.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/api/lmserver/ns-lmserver-server_info_1017">SERVER_INFO_1017</a>



<a href="/windows/desktop/api/lmserver/ns-lmserver-server_info_102">SERVER_INFO_102</a>



<a href="/windows/desktop/NetMgmt/server-functions">Server Functions</a>