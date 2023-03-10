---
UID: NS:http._HTTP_SERVICE_CONFIG_SSL_QUERY
title: HTTP_SERVICE_CONFIG_SSL_QUERY (http.h)
description: Used to specify a particular record to query in the SSL configuration store.
helpviewer_keywords: ["*PHTTP_SERVICE_CONFIG_SSL_QUERY","HTTP_SERVICE_CONFIG_SSL_QUERY","HTTP_SERVICE_CONFIG_SSL_QUERY structure [HTTP]","PHTTP_SERVICE_CONFIG_SSL_QUERY","PHTTP_SERVICE_CONFIG_SSL_QUERY structure pointer [HTTP]","_http_http_service_config_ssl_query","http.http_service_config_ssl_query","http/HTTP_SERVICE_CONFIG_SSL_QUERY","http/PHTTP_SERVICE_CONFIG_SSL_QUERY"]
old-location: http\http_service_config_ssl_query.htm
tech.root: http
ms.assetid: 733b451a-d35b-4b83-ba49-0529309cd99b
ms.date: 12/05/2018
ms.keywords: '*PHTTP_SERVICE_CONFIG_SSL_QUERY, HTTP_SERVICE_CONFIG_SSL_QUERY, HTTP_SERVICE_CONFIG_SSL_QUERY structure [HTTP], PHTTP_SERVICE_CONFIG_SSL_QUERY, PHTTP_SERVICE_CONFIG_SSL_QUERY structure pointer [HTTP], _http_http_service_config_ssl_query, http.http_service_config_ssl_query, http/HTTP_SERVICE_CONFIG_SSL_QUERY, http/PHTTP_SERVICE_CONFIG_SSL_QUERY'
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
req.typenames: HTTP_SERVICE_CONFIG_SSL_QUERY, *PHTTP_SERVICE_CONFIG_SSL_QUERY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_SERVICE_CONFIG_SSL_QUERY
 - http/_HTTP_SERVICE_CONFIG_SSL_QUERY
 - PHTTP_SERVICE_CONFIG_SSL_QUERY
 - http/PHTTP_SERVICE_CONFIG_SSL_QUERY
 - HTTP_SERVICE_CONFIG_SSL_QUERY
 - http/HTTP_SERVICE_CONFIG_SSL_QUERY
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
 - HTTP_SERVICE_CONFIG_SSL_QUERY
---

# HTTP_SERVICE_CONFIG_SSL_QUERY structure


## -description

The 
<b>HTTP_SERVICE_CONFIG_SSL_QUERY</b> structure is used to specify a particular record to query in the SSL configuration store. It is passed to the 
<a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a> function using the <i>pInputConfigInfo</i> parameter when the <i>ConfigId</i> parameter is set to <b>HttpServiceConfigSSLCertInfo</b>.

## -struct-fields

### -field QueryDesc

One of the  following values from the <a href="/windows/desktop/api/http/ne-http-http_service_config_query_type">HTTP_SERVICE_CONFIG_QUERY_TYPE</a> enumeration. 







#### HttpServiceConfigQueryExact

Returns a single SSL record.



#### HttpServiceConfigQueryNext

Returns a sequence of SSL records in a sequence of calls, as controlled by the <i>dwToken</i> parameter.

### -field KeyDesc

If the <i>QueryDesc</i> parameter is equal to <b>HttpServiceConfigQueryExact</b>, then <i>KeyDesc</i> should contain an 
<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_key">HTTP_SERVICE_CONFIG_SSL_KEY</a> structure that identifies the SSL certificate record queried. If the <i>QueryDesc</i> parameter is equal to HTTPServiceConfigQueryNext, then <i>KeyDesc</i> is ignored.

### -field dwToken

If the <i>QueryDesc</i> parameter is equal to <b>HTTPServiceConfigQueryNext</b>, then <i>dwToken</i> must be equal to zero on the first call to the 
<a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a> function, one on the second call, two on the third call, and so forth until all SSL certificate records are returned, at which point 
<b>HttpQueryServiceConfiguration</b> returns ERROR_NO_MORE_ITEMS. 




If the <i>QueryDesc</i> parameter is equal to <b>HttpServiceConfigQueryExact</b>, then <i>dwToken</i> is ignored.

## -see-also

<a href="/windows/desktop/api/http/ne-http-http_service_config_query_type">HTTP_SERVICE_CONFIG_QUERY_TYPE</a>



<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_set">HTTP_SERVICE_CONFIG_SSL_SET</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a>