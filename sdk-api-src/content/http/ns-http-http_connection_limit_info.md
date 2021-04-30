---
UID: NS:http._HTTP_CONNECTION_LIMIT_INFO
title: HTTP_CONNECTION_LIMIT_INFO (http.h)
description: Used to set or query the limit on the maximum number of outstanding connections for a URL Group.
helpviewer_keywords: ["*PHTTP_CONNECTION_LIMIT_INFO","*PHTTP_CONNECTION_LIMIT_INFO structure [HTTP]","HTTP_CONNECTION_LIMIT_INFO","HTTP_CONNECTION_LIMIT_INFO structure [HTTP]","http.http_connection_limit_info","http/*PHTTP_CONNECTION_LIMIT_INFO","http/HTTP_CONNECTION_LIMIT_INFO"]
old-location: http\http_connection_limit_info.htm
tech.root: http
ms.assetid: 6d2c1eeb-d248-4ca5-80b3-5c9f69ce8b9b
ms.date: 12/05/2018
ms.keywords: '*PHTTP_CONNECTION_LIMIT_INFO, *PHTTP_CONNECTION_LIMIT_INFO structure [HTTP], HTTP_CONNECTION_LIMIT_INFO, HTTP_CONNECTION_LIMIT_INFO structure [HTTP], http.http_connection_limit_info, http/*PHTTP_CONNECTION_LIMIT_INFO, http/HTTP_CONNECTION_LIMIT_INFO'
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: HTTP_CONNECTION_LIMIT_INFO, *PHTTP_CONNECTION_LIMIT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_CONNECTION_LIMIT_INFO
 - http/_HTTP_CONNECTION_LIMIT_INFO
 - PHTTP_CONNECTION_LIMIT_INFO
 - http/PHTTP_CONNECTION_LIMIT_INFO
 - HTTP_CONNECTION_LIMIT_INFO
 - http/HTTP_CONNECTION_LIMIT_INFO
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
 - HTTP_CONNECTION_LIMIT_INFO
---

# HTTP_CONNECTION_LIMIT_INFO structure


## -description

The <b>HTTP_CONNECTION_LIMIT_INFO</b> structure is used to set or query  the limit on the  maximum number of outstanding connections for a URL Group.

 This structure must be used when setting or querying the <a href="/windows/desktop/api/http/ne-http-http_server_property">HttpServerConnectionsProperty</a> on a URL Group.

## -struct-fields

### -field Flags

The <a href="/windows/desktop/api/http/ns-http-http_property_flags">HTTP_PROPERTY_FLAGS</a> structure specifying whether the property is present.

### -field MaxConnections

The number of connections allowed. Setting this value to HTTP_LIMIT_INFINITE allows an unlimited number of connections.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-structures">HTTP Server API Version 2.0 Structures</a>



<a href="/windows/desktop/api/http/ne-http-http_server_property">HTTP_SERVER_PROPERTY</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryurlgroupproperty">HttpQueryUrlGroupProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpseturlgroupproperty">HttpSetUrlGroupProperty</a>