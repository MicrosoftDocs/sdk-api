---
UID: NS:http._HTTP_SERVICE_CONFIG_SSL_KEY
title: HTTP_SERVICE_CONFIG_SSL_KEY (http.h)
description: Serves as the key by which a given Secure Sockets Layer (SSL) certificate record is identified.
helpviewer_keywords: ["*PHTTP_SERVICE_CONFIG_SSL_KEY","HTTP_SERVICE_CONFIG_SSL_KEY","HTTP_SERVICE_CONFIG_SSL_KEY structure [HTTP]","PHTTP_SERVICE_CONFIG_SSL_KEY","PHTTP_SERVICE_CONFIG_SSL_KEY structure pointer [HTTP]","_http_http_service_config_ssl_key","http.http_service_config_ssl_key","http/HTTP_SERVICE_CONFIG_SSL_KEY","http/PHTTP_SERVICE_CONFIG_SSL_KEY"]
old-location: http\http_service_config_ssl_key.htm
tech.root: http
ms.assetid: 67231fa5-69eb-4353-8c3c-326ec9095554
ms.date: 12/05/2018
ms.keywords: '*PHTTP_SERVICE_CONFIG_SSL_KEY, HTTP_SERVICE_CONFIG_SSL_KEY, HTTP_SERVICE_CONFIG_SSL_KEY structure [HTTP], PHTTP_SERVICE_CONFIG_SSL_KEY, PHTTP_SERVICE_CONFIG_SSL_KEY structure pointer [HTTP], _http_http_service_config_ssl_key, http.http_service_config_ssl_key, http/HTTP_SERVICE_CONFIG_SSL_KEY, http/PHTTP_SERVICE_CONFIG_SSL_KEY'
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
req.typenames: HTTP_SERVICE_CONFIG_SSL_KEY, *PHTTP_SERVICE_CONFIG_SSL_KEY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_SERVICE_CONFIG_SSL_KEY
 - http/_HTTP_SERVICE_CONFIG_SSL_KEY
 - PHTTP_SERVICE_CONFIG_SSL_KEY
 - http/PHTTP_SERVICE_CONFIG_SSL_KEY
 - HTTP_SERVICE_CONFIG_SSL_KEY
 - http/HTTP_SERVICE_CONFIG_SSL_KEY
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
 - HTTP_SERVICE_CONFIG_SSL_KEY
---

# HTTP_SERVICE_CONFIG_SSL_KEY structure


## -description

The 
<b>HTTP_SERVICE_CONFIG_SSL_KEY</b> structure serves as the key by which a given Secure Sockets Layer (SSL) certificate record is identified. It appears in the 
<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_set">HTTP_SERVICE_CONFIG_SSL_SET</a> and the 
<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_query">HTTP_SERVICE_CONFIG_SSL_QUERY</a> structures, and is passed as the <i>pConfigInformation</i> parameter to 
<a href="/windows/desktop/api/http/nf-http-httpdeleteserviceconfiguration">HTTPDeleteServiceConfiguration</a>, 
<a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a>, and 
<a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HttpSetServiceConfiguration</a> when the <i>ConfigId</i> parameter is set to <b>HttpServiceConfigSSLCertInfo</b>.

## -struct-fields

### -field pIpPort

Pointer to a <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure that contains the Internet Protocol (IP) address with which this SSL certificate is associated.

If the <b>sin_addr</b> field in <b>IpPort</b> is set to 0.0.0.0, the certificate is applicable to all IPv4 and IPv6 addresses.
   If the <b>sin6_addr</b> field in <b>IpPort</b> is set to [::], the certificate is applicable to all IPv6 addresses.

## -see-also

<a href="/windows/desktop/api/http/nf-http-httpdeleteserviceconfiguration">HTTPDeleteServiceConfiguration</a>



<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_query">HTTP_SERVICE_CONFIG_SSL_QUERY</a>



<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_set">HTTP_SERVICE_CONFIG_SSL_SET</a>