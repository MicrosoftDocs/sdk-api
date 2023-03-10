---
UID: NE:http._HTTP_SERVICE_CONFIG_CACHE_KEY
title: HTTP_SERVICE_CONFIG_CACHE_KEY (http.h)
description: Used in the HttpSetServiceConfiguration and HttpQueryServiceConfiguration functions.
helpviewer_keywords: ["*PHTTP_SERVICE_CONFIG_CACHE_KEY","CacheRangeChunkSize","HTTP_SERVICE_CONFIG_CACHE_KEY","HTTP_SERVICE_CONFIG_CACHE_KEY enumeration [HTTP]","MaxCacheResponseSize","http.http_service_config_cache_key","http/CacheRangeChunkSize","http/HTTP_SERVICE_CONFIG_CACHE_KEY","http/MaxCacheResponseSize"]
old-location: http\http_service_config_cache_key.htm
tech.root: http
ms.assetid: 796b93ab-742b-4e18-a522-6938fbf78786
ms.date: 12/05/2018
ms.keywords: '*PHTTP_SERVICE_CONFIG_CACHE_KEY, CacheRangeChunkSize, HTTP_SERVICE_CONFIG_CACHE_KEY, HTTP_SERVICE_CONFIG_CACHE_KEY enumeration [HTTP], MaxCacheResponseSize, http.http_service_config_cache_key, http/CacheRangeChunkSize, http/HTTP_SERVICE_CONFIG_CACHE_KEY, http/MaxCacheResponseSize'
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: HTTP_SERVICE_CONFIG_CACHE_KEY, *PHTTP_SERVICE_CONFIG_CACHE_KEY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_SERVICE_CONFIG_CACHE_KEY
 - http/_HTTP_SERVICE_CONFIG_CACHE_KEY
 - PHTTP_SERVICE_CONFIG_CACHE_KEY
 - http/PHTTP_SERVICE_CONFIG_CACHE_KEY
 - HTTP_SERVICE_CONFIG_CACHE_KEY
 - http/HTTP_SERVICE_CONFIG_CACHE_KEY
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
 - HTTP_SERVICE_CONFIG_CACHE_KEY
---

# HTTP_SERVICE_CONFIG_CACHE_KEY enumeration


## -description

 Used in the <a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HttpSetServiceConfiguration</a> and <a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a> functions.

## -enum-fields

### -field MaxCacheResponseSize:0

The maximum cache size for the response.

### -field CacheRangeChunkSize

The chunk size.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-enumeration-types">HTTP Server API Version 2.0 Enumeration Types</a>
