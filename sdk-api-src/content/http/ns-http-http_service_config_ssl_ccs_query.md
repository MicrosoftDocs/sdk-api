---
UID: NS:http._HTTP_SERVICE_CONFIG_SSL_CCS_QUERY
title: HTTP_SERVICE_CONFIG_SSL_CCS_QUERY (http.h)
description: Specifies a Secure Sockets Layer (SSL) configuration to query for an SSL Centralized Certificate Store (CCS) record on the port when you call the HttpQueryServiceConfiguration function.
helpviewer_keywords: ["*PHTTP_SERVICE_CONFIG_SSL_CCS_QUERY","HTTP_SERVICE_CONFIG_SSL_CCS_QUERY","HTTP_SERVICE_CONFIG_SSL_CCS_QUERY structure [HTTP]","HttpServiceConfigQueryExact","HttpServiceConfigQueryNext","PHTTP_SERVICE_CONFIG_SSL_CCS_QUERY","PHTTP_SERVICE_CONFIG_SSL_CCS_QUERY structure pointer [HTTP]","http.http_service_config_ssl_ccs_query","http/HTTP_SERVICE_CONFIG_SSL_CCS_QUERY","http/PHTTP_SERVICE_CONFIG_SSL_CCS_QUERY"]
old-location: http\http_service_config_ssl_ccs_query.htm
tech.root: http
ms.assetid: E7578D74-E8BE-472D-A01B-51BBA511F561
ms.date: 12/05/2018
ms.keywords: '*PHTTP_SERVICE_CONFIG_SSL_CCS_QUERY, HTTP_SERVICE_CONFIG_SSL_CCS_QUERY, HTTP_SERVICE_CONFIG_SSL_CCS_QUERY structure [HTTP], HttpServiceConfigQueryExact, HttpServiceConfigQueryNext, PHTTP_SERVICE_CONFIG_SSL_CCS_QUERY, PHTTP_SERVICE_CONFIG_SSL_CCS_QUERY structure pointer [HTTP], http.http_service_config_ssl_ccs_query, http/HTTP_SERVICE_CONFIG_SSL_CCS_QUERY, http/PHTTP_SERVICE_CONFIG_SSL_CCS_QUERY'
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: HTTP_SERVICE_CONFIG_SSL_CCS_QUERY, *PHTTP_SERVICE_CONFIG_SSL_CCS_QUERY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_SERVICE_CONFIG_SSL_CCS_QUERY
 - http/_HTTP_SERVICE_CONFIG_SSL_CCS_QUERY
 - PHTTP_SERVICE_CONFIG_SSL_CCS_QUERY
 - http/PHTTP_SERVICE_CONFIG_SSL_CCS_QUERY
 - HTTP_SERVICE_CONFIG_SSL_CCS_QUERY
 - http/HTTP_SERVICE_CONFIG_SSL_CCS_QUERY
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
 - HTTP_SERVICE_CONFIG_SSL_CCS_QUERY
---

# HTTP_SERVICE_CONFIG_SSL_CCS_QUERY structure


## -description

Specifies a Secure Sockets Layer (SSL) configuration to query for an SSL Centralized Certificate Store (CCS) record on the port when you call the <a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a> function. The   SSL certificate record specifies that Http.sys should consult the CCS store to find certificates if the port receives a Transport Layer Security (TLS) handshake.

## -struct-fields

### -field QueryDesc

One of the following values from the <a href="/windows/desktop/api/http/ne-http-http_service_config_query_type">HTTP_SERVICE_CONFIG_QUERY_TYPE</a> enumeration that indicates whether the call to <a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a> is a call to retrieve a single record or part of a sequence of calls to retrieve a sequence of records.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigQueryExact"></a><a id="httpserviceconfigqueryexact"></a><a id="HTTPSERVICECONFIGQUERYEXACT"></a><dl>
<dt><b>HttpServiceConfigQueryExact</b></dt>
</dl>
</td>
<td width="60%">
The call to <a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a> is call to retrieve a single SSL CCS certificate record, which the <b>KeyDesc</b> member specifies.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigQueryNext"></a><a id="httpserviceconfigquerynext"></a><a id="HTTPSERVICECONFIGQUERYNEXT"></a><dl>
<dt><b>HttpServiceConfigQueryNext</b></dt>
</dl>
</td>
<td width="60%">
The call to <a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a> is part of  a sequence of calls to retrieve a sequence of SSL CCS certificate records. The value of the <b>dwToken</b> member controls which record in the sequence that this call to <b>HttpQueryServiceConfiguration</b> retrieves.

</td>
</tr>
</table>

### -field KeyDesc

An <a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_ccs_key">HTTP_SERVICE_CONFIG_SSL_CCS_KEY</a> structure that identifies the SSL CCS certificate record queried,  if the <b>QueryDesc</b> member is equal to <b>HttpServiceConfigQueryExact</b>. Ignored if <b>QueryDesc</b>  is equal to <b>HTTPServiceConfigQueryNext</b>.

### -field dwToken

The position of the record in the sequence of records that this call to <a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a> should retrieve if the <b>QueryDesc</b> method equals <b>HTTPServiceConfigQueryNext</b>, starting from zero.  In other words,  <b>dwToken</b> must be equal to zero on the first call to the <b>HttpQueryServiceConfiguration</b> function, one on the second call, two on the third call, and so forth. When the sequence of calls has returned  all SSL certificate records,  <b>HttpQueryServiceConfiguration</b> returns <b>ERROR_NO_MORE_ITEMS</b>.
Ignored if the <b>QueryDesc</b> is equal to <b>HttpServiceConfigQueryExact</b>.

## -remarks

Pass this structure to the <a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a> function by using the <i>pInputConfigInfo</i> parameter when the <i>ConfigId</i> parameter is set to <b>HttpServiceConfigSslCcsCertInfo</b>.

## -see-also

<a href="/windows/desktop/api/http/ne-http-http_service_config_query_type">HTTP_SERVICE_CONFIG_QUERY_TYPE</a>



<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_ccs_key">HTTP_SERVICE_CONFIG_SSL_CCS_KEY</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a>