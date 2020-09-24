---
UID: NS:http._HTTP_SERVICE_CONFIG_SSL_SNI_QUERY
title: HTTP_SERVICE_CONFIG_SSL_SNI_QUERY (http.h)
description: Used to specify a particular Secure Sockets Layer (SSL) Server Name Indication (SNI) certificate record to query in the SSL SNI store.
helpviewer_keywords: ["*PHTTP_SERVICE_CONFIG_SSL_SNI_QUERY","HTTP_SERVICE_CONFIG_SSL_SNI_QUERY","HTTP_SERVICE_CONFIG_SSL_SNI_QUERY structure [HTTP]","HttpServiceConfigQueryExact","HttpServiceConfigQueryNext","PHTTP_SERVICE_CONFIG_SSL_SNI_QUERY","PHTTP_SERVICE_CONFIG_SSL_SNI_QUERY structure pointer [HTTP]","http.http_service_config_ssl_sni_query","http/HTTP_SERVICE_CONFIG_SSL_SNI_QUERY","http/PHTTP_SERVICE_CONFIG_SSL_SNI_QUERY"]
old-location: http\http_service_config_ssl_sni_query.htm
tech.root: http
ms.assetid: 9C45B1B1-5572-4153-BBA4-0E8A52F650CA
ms.date: 12/05/2018
ms.keywords: '*PHTTP_SERVICE_CONFIG_SSL_SNI_QUERY, HTTP_SERVICE_CONFIG_SSL_SNI_QUERY, HTTP_SERVICE_CONFIG_SSL_SNI_QUERY structure [HTTP], HttpServiceConfigQueryExact, HttpServiceConfigQueryNext, PHTTP_SERVICE_CONFIG_SSL_SNI_QUERY, PHTTP_SERVICE_CONFIG_SSL_SNI_QUERY structure pointer [HTTP], http.http_service_config_ssl_sni_query, http/HTTP_SERVICE_CONFIG_SSL_SNI_QUERY, http/PHTTP_SERVICE_CONFIG_SSL_SNI_QUERY'
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
req.typenames: HTTP_SERVICE_CONFIG_SSL_SNI_QUERY, *PHTTP_SERVICE_CONFIG_SSL_SNI_QUERY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_SERVICE_CONFIG_SSL_SNI_QUERY
 - http/_HTTP_SERVICE_CONFIG_SSL_SNI_QUERY
 - PHTTP_SERVICE_CONFIG_SSL_SNI_QUERY
 - http/PHTTP_SERVICE_CONFIG_SSL_SNI_QUERY
 - HTTP_SERVICE_CONFIG_SSL_SNI_QUERY
 - http/HTTP_SERVICE_CONFIG_SSL_SNI_QUERY
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
 - HTTP_SERVICE_CONFIG_SSL_SNI_QUERY
---

# HTTP_SERVICE_CONFIG_SSL_SNI_QUERY structure


## -description

The 
<b>HTTP_SERVICE_CONFIG_SSL_SNI_QUERY</b> structure is used to specify a particular Secure Sockets Layer (SSL) Server Name Indication (SNI) certificate record to query in the SSL SNI store. It is passed to the 
<a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a> function using the <i>pInputConfigInfo</i> parameter when the <i>ConfigId</i> parameter is set to <b>HttpServiceConfigSslSniCertInfo</b>.

## -struct-fields

### -field QueryDesc

One of the  following values from the <a href="/windows/desktop/api/http/ne-http-http_service_config_query_type">HTTP_SERVICE_CONFIG_QUERY_TYPE</a> enumeration. 


					

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
Returns a single SSL SNI certificate record.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigQueryNext"></a><a id="httpserviceconfigquerynext"></a><a id="HTTPSERVICECONFIGQUERYNEXT"></a><dl>
<dt><b>HttpServiceConfigQueryNext</b></dt>
</dl>
</td>
<td width="60%">
Returns a sequence of SSL SNI certificate records in a sequence of calls, as controlled by <i>dwToken</i>.

</td>
</tr>
</table>

### -field KeyDesc

If the <i>QueryDesc</i> parameter is equal to <b>HttpServiceConfigQueryExact</b>, then <i>KeyDesc</i> should contain an 
<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_sni_key">HTTP_SERVICE_CONFIG_SSL_SNI_KEY</a> structure that identifies the SSL SNI certificate record queried. If the <i>QueryDesc</i> parameter is equal to <b>HTTPServiceConfigQueryNext</b>, then <i>KeyDesc</i> is ignored.

### -field dwToken

If the <i>QueryDesc</i> parameter is equal to <b>HTTPServiceConfigQueryNext</b>, then <i>dwToken</i> must be equal to zero on the first call to the 
<a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a> function, one on the second call, two on the third call, and so forth until all SSL certificate records are returned, at which point 
<b>HttpQueryServiceConfiguration</b> returns ERROR_NO_MORE_ITEMS. 




If the <i>QueryDesc</i> parameter is equal to <b>HttpServiceConfigQueryExact</b>, then <i>dwToken</i> is ignored.

## -see-also

<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_sni_key">HTTP_SERVICE_CONFIG_SSL_SNI_KEY</a>



<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_sni_set">HTTP_SERVICE_CONFIG_SSL_SNI_SET</a>



<a href="/windows/desktop/api/http/nf-http-httpdeleteserviceconfiguration">HttpDeleteServiceConfiguration</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a>



<a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HttpSetServiceConfiguration</a>