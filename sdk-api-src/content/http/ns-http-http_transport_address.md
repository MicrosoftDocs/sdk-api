---
UID: NS:http._HTTP_TRANSPORT_ADDRESS
title: HTTP_TRANSPORT_ADDRESS (http.h)
description: Specifies the addresses (local and remote) used for a particular HTTP connection.
helpviewer_keywords: ["*PHTTP_TRANSPORT_ADDRESS","HTTP_TRANSPORT_ADDRESS","HTTP_TRANSPORT_ADDRESS structure [HTTP]","PHTTP_TRANSPORT_ADDRESS","PHTTP_TRANSPORT_ADDRESS structure pointer [HTTP]","_http_http_transport_address","http.http_transport_address","http/HTTP_TRANSPORT_ADDRESS","http/PHTTP_TRANSPORT_ADDRESS"]
old-location: http\http_transport_address.htm
tech.root: http
ms.assetid: 2dac2817-c911-4ca1-afb1-32147a16ad4c
ms.date: 12/05/2018
ms.keywords: '*PHTTP_TRANSPORT_ADDRESS, HTTP_TRANSPORT_ADDRESS, HTTP_TRANSPORT_ADDRESS structure [HTTP], PHTTP_TRANSPORT_ADDRESS, PHTTP_TRANSPORT_ADDRESS structure pointer [HTTP], _http_http_transport_address, http.http_transport_address, http/HTTP_TRANSPORT_ADDRESS, http/PHTTP_TRANSPORT_ADDRESS'
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: HTTP_TRANSPORT_ADDRESS, *PHTTP_TRANSPORT_ADDRESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_TRANSPORT_ADDRESS
 - http/_HTTP_TRANSPORT_ADDRESS
 - PHTTP_TRANSPORT_ADDRESS
 - http/PHTTP_TRANSPORT_ADDRESS
 - HTTP_TRANSPORT_ADDRESS
 - http/HTTP_TRANSPORT_ADDRESS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_TRANSPORT_ADDRESS
---

# HTTP_TRANSPORT_ADDRESS structure


## -description

The 
<b>HTTP_TRANSPORT_ADDRESS</b> structure specifies the addresses (local and remote) used for a particular HTTP connection.

## -struct-fields

### -field pRemoteAddress

A pointer to the remote IP address associated with this connection. For more information about how to access this address, see the Remarks section.

### -field pLocalAddress

A pointer to the local IP address associated with this connection. For more information about how to access this address, see the Remarks section.

## -remarks

Although the <b>pRemoteAddress</b> and <b>pLocalAddress</b> members are formally declared as <b>PSOCKADDR</b>, they are in fact <b>PSOCKADDR_IN</b> or <b>PSOCKADDR_IN6</b> types. Inspect the <b>sa_family</b> member, which is the same in all three structures, to determine how to access the address. If <b>sa_family</b> is equal to AF_INET, then the address is in IPv4 form and can be accessed by casting the members to <b>PSOCKADDR_IN</b>, but if <b>sa_family</b> equals AF_INET6, the address is in IPv6 form and you must cast them to <b>PSOCKADDR_IN6</b> before accessing the address. Both <b>pLocalAddress</b> and <b>pRemoteAddress</b> are always of the same type; that is they are either both of type <b>PSOCKADDR_IN</b> or both of type <b>PSOCKADDR_IN6</b>.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-1-0-structures">HTTP Server API Version 1.0 Structures</a>



<a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a>