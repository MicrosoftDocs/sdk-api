---
UID: NS:http._HTTP_BANDWIDTH_LIMIT_INFO
title: HTTP_BANDWIDTH_LIMIT_INFO (http.h)
description: The HTTP_BANDWIDTH_LIMIT_INFO structure is used to set or query the bandwidth throttling limit. This structure must be used when setting or querying the HttpServerBandwidthProperty on a URL Group or server session.
helpviewer_keywords: ["*PHTTP_BANDWIDTH_LIMIT_INFO","*PHTTP_BANDWIDTH_LIMIT_INFO structure [HTTP]","HTTP_BANDWIDTH_LIMIT_INFO","HTTP_BANDWIDTH_LIMIT_INFO structure [HTTP]","http.http_bandwidth_limit_info","http/*PHTTP_BANDWIDTH_LIMIT_INFO","http/HTTP_BANDWIDTH_LIMIT_INFO"]
old-location: http\http_bandwidth_limit_info.htm
tech.root: http
ms.assetid: 34c85ecf-1eb4-4f0d-a081-4b9feeb8dd15
ms.date: 12/05/2018
ms.keywords: '*PHTTP_BANDWIDTH_LIMIT_INFO, *PHTTP_BANDWIDTH_LIMIT_INFO structure [HTTP], HTTP_BANDWIDTH_LIMIT_INFO, HTTP_BANDWIDTH_LIMIT_INFO structure [HTTP], http.http_bandwidth_limit_info, http/*PHTTP_BANDWIDTH_LIMIT_INFO, http/HTTP_BANDWIDTH_LIMIT_INFO'
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
req.typenames: HTTP_BANDWIDTH_LIMIT_INFO, *PHTTP_BANDWIDTH_LIMIT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_BANDWIDTH_LIMIT_INFO
 - http/_HTTP_BANDWIDTH_LIMIT_INFO
 - PHTTP_BANDWIDTH_LIMIT_INFO
 - http/PHTTP_BANDWIDTH_LIMIT_INFO
 - HTTP_BANDWIDTH_LIMIT_INFO
 - http/HTTP_BANDWIDTH_LIMIT_INFO
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
 - HTTP_BANDWIDTH_LIMIT_INFO
---

# HTTP_BANDWIDTH_LIMIT_INFO structure


## -description

The <b>HTTP_BANDWIDTH_LIMIT_INFO</b> structure  is used to set or query the bandwidth throttling limit. 

This structure must be used when setting or querying the <a href="/windows/desktop/api/http/ne-http-http_server_property">HttpServerBandwidthProperty</a> on a URL Group or server session.

## -struct-fields

### -field Flags

The <a href="/windows/desktop/api/http/ns-http-http_property_flags">HTTP_PROPERTY_FLAGS</a> structure specifying whether the property is present.

### -field MaxBandwidth

The maximum allowed bandwidth rate in bytesper second. Setting the value to HTTP_LIMIT_INFINITE  allows unlimited bandwidth rate. The value cannot be smaller than HTTP_MIN_ALLOWED_BANDWIDTH_THROTTLING_RATE.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-structures">HTTP Server API Version 2.0 Structures</a>



<a href="/windows/desktop/api/http/ne-http-http_server_property">HTTP_SERVER_PROPERTY</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryserversessionproperty">HttpQueryServerSessionProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryurlgroupproperty">HttpQueryUrlGroupProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpsetserversessionproperty">HttpSetServerSessionProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpseturlgroupproperty">HttpSetUrlGroupProperty</a>