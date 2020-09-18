---
UID: NE:http._HTTP_SERVICE_CONFIG_QUERY_TYPE
title: HTTP_SERVICE_CONFIG_QUERY_TYPE (http.h)
description: The HTTP_SERVICE_CONFIG_QUERY_TYPE enumeration type defines various types of queries to make. It is used in the HTTP_SERVICE_CONFIG_SSL_QUERY, HTTP_SERVICE_CONFIG_SSL_CCS_QUERY, and HTTP_SERVICE_CONFIG_URLACL_QUERY structures.
helpviewer_keywords: ["*PHTTP_SERVICE_CONFIG_QUERY_TYPE","HTTP_SERVICE_CONFIG_QUERY_TYPE","HTTP_SERVICE_CONFIG_QUERY_TYPE enumeration [HTTP]","HttpServiceConfigQueryExact","HttpServiceConfigQueryMax","HttpServiceConfigQueryNext","PHTTP_SERVICE_CONFIG_QUERY_TYPE","PHTTP_SERVICE_CONFIG_QUERY_TYPE enumeration pointer [HTTP]","_http_http_service_config_query_type","http.http_service_config_query_type","http/HTTP_SERVICE_CONFIG_QUERY_TYPE","http/HttpServiceConfigQueryExact","http/HttpServiceConfigQueryMax","http/HttpServiceConfigQueryNext","http/PHTTP_SERVICE_CONFIG_QUERY_TYPE"]
old-location: http\http_service_config_query_type.htm
tech.root: http
ms.assetid: 63b2503f-7e71-4c62-8e9c-ad0f5103a9e8
ms.date: 12/05/2018
ms.keywords: '*PHTTP_SERVICE_CONFIG_QUERY_TYPE, HTTP_SERVICE_CONFIG_QUERY_TYPE, HTTP_SERVICE_CONFIG_QUERY_TYPE enumeration [HTTP], HttpServiceConfigQueryExact, HttpServiceConfigQueryMax, HttpServiceConfigQueryNext, PHTTP_SERVICE_CONFIG_QUERY_TYPE, PHTTP_SERVICE_CONFIG_QUERY_TYPE enumeration pointer [HTTP], _http_http_service_config_query_type, http.http_service_config_query_type, http/HTTP_SERVICE_CONFIG_QUERY_TYPE, http/HttpServiceConfigQueryExact, http/HttpServiceConfigQueryMax, http/HttpServiceConfigQueryNext, http/PHTTP_SERVICE_CONFIG_QUERY_TYPE'
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
req.typenames: HTTP_SERVICE_CONFIG_QUERY_TYPE, *PHTTP_SERVICE_CONFIG_QUERY_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_SERVICE_CONFIG_QUERY_TYPE
 - http/_HTTP_SERVICE_CONFIG_QUERY_TYPE
 - PHTTP_SERVICE_CONFIG_QUERY_TYPE
 - http/PHTTP_SERVICE_CONFIG_QUERY_TYPE
 - HTTP_SERVICE_CONFIG_QUERY_TYPE
 - http/HTTP_SERVICE_CONFIG_QUERY_TYPE
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
 - HTTP_SERVICE_CONFIG_QUERY_TYPE
---

# HTTP_SERVICE_CONFIG_QUERY_TYPE enumeration


## -description

The 
<b>HTTP_SERVICE_CONFIG_QUERY_TYPE</b> enumeration type defines various types of queries to make. It is used in the 
<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_query">HTTP_SERVICE_CONFIG_SSL_QUERY</a>, <a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_ccs_query">HTTP_SERVICE_CONFIG_SSL_CCS_QUERY</a>, and 
<a href="/windows/desktop/api/http/ns-http-http_service_config_urlacl_query">HTTP_SERVICE_CONFIG_URLACL_QUERY</a> structures.

## -enum-fields

### -field HttpServiceConfigQueryExact

The query returns a single record that matches the specified key value.

### -field HttpServiceConfigQueryNext

The query iterates through the store and returns all records in sequence, using an index value that the calling process increments between query calls.

### -field HttpServiceConfigQueryMax

Terminates the enumeration; is not used to define a query type.

## -see-also

<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_ccs_query">HTTP_SERVICE_CONFIG_SSL_CCS_QUERY</a>



<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_query">HTTP_SERVICE_CONFIG_SSL_QUERY</a>



<a href="/windows/desktop/api/http/ns-http-http_service_config_urlacl_query">HTTP_SERVICE_CONFIG_URLACL_QUERY</a>