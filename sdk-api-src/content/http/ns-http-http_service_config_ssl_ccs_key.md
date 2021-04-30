---
UID: NS:http._HTTP_SERVICE_CONFIG_SSL_CCS_KEY
title: HTTP_SERVICE_CONFIG_SSL_CCS_KEY (http.h)
description: Serves as the key by which identifies the SSL certificate record that specifies that Http.sys should consult the Centralized Certificate Store (CCS) store to find certificates if the port receives a Transport Layer Security (TLS) handshake.
helpviewer_keywords: ["*PHTTP_SERVICE_CONFIG_SSL_CCS_KEY","HTTP_SERVICE_CONFIG_SSL_CCS_KEY","HTTP_SERVICE_CONFIG_SSL_CCS_KEY structure [HTTP]","PHTTP_SERVICE_CONFIG_SSL_CCS_KEY","PHTTP_SERVICE_CONFIG_SSL_CCS_KEY structure pointer [HTTP]","http.http_service_config_ssl_ccs_key","http/HTTP_SERVICE_CONFIG_SSL_CCS_KEY","http/PHTTP_SERVICE_CONFIG_SSL_CCS_KEY"]
old-location: http\http_service_config_ssl_ccs_key.htm
tech.root: http
ms.assetid: C40070D6-AE19-4E42-A7C6-38F8AF5C1F53
ms.date: 12/05/2018
ms.keywords: '*PHTTP_SERVICE_CONFIG_SSL_CCS_KEY, HTTP_SERVICE_CONFIG_SSL_CCS_KEY, HTTP_SERVICE_CONFIG_SSL_CCS_KEY structure [HTTP], PHTTP_SERVICE_CONFIG_SSL_CCS_KEY, PHTTP_SERVICE_CONFIG_SSL_CCS_KEY structure pointer [HTTP], http.http_service_config_ssl_ccs_key, http/HTTP_SERVICE_CONFIG_SSL_CCS_KEY, http/PHTTP_SERVICE_CONFIG_SSL_CCS_KEY'
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
req.typenames: HTTP_SERVICE_CONFIG_SSL_CCS_KEY, *PHTTP_SERVICE_CONFIG_SSL_CCS_KEY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_SERVICE_CONFIG_SSL_CCS_KEY
 - http/_HTTP_SERVICE_CONFIG_SSL_CCS_KEY
 - PHTTP_SERVICE_CONFIG_SSL_CCS_KEY
 - http/PHTTP_SERVICE_CONFIG_SSL_CCS_KEY
 - HTTP_SERVICE_CONFIG_SSL_CCS_KEY
 - http/HTTP_SERVICE_CONFIG_SSL_CCS_KEY
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
 - HTTP_SERVICE_CONFIG_SSL_CCS_KEY
---

# HTTP_SERVICE_CONFIG_SSL_CCS_KEY structure


## -description

Serves as the key by which identifies the   SSL certificate record that specifies that Http.sys should consult the Centralized Certificate Store (CCS) store to find certificates if the port receives a Transport Layer Security (TLS) handshake.

## -struct-fields

### -field LocalAddress

A <a href="/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)">SOCKADDR_STORAGE</a> structure that contains the Internet Protocol version 4 (IPv4) address with which this SSL certificate record is associated. It must be set to the IPv4 wildcard address of type <a href="/windows/desktop/api/ws2def/ns-ws2def-sockaddr_in">SOCKADDR_IN</a> with the <b>sin_family</b> member set to AF_INET and the <b>sin_addr</b> member filled with zeros (0.0.0.0). The <b>sin_port</b> member can be any valid port.

## -remarks

 The <b>HTTP_SERVICE_CONFIG_SSL_CCS_KEY</b> structure appears in the <a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_ccs_set">HTTP_SERVICE_CONFIG_SSL_CCS_SET</a> and the <a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_ccs_query">HTTP_SERVICE_CONFIG_SSL_CCS_QUERY</a> structures. <b>HTTP_SERVICE_CONFIG_SSL_CCS_KEY</b> is passed as part of these structures in the <i>pConfigInformation</i>, <i>ConfigInfo</i>, <i>pInputConfigInfo</i>, and <i>pOutputConfigInfo</i> parameters to the <a href="/windows/desktop/api/http/nf-http-httpdeleteserviceconfiguration">HttpDeleteServiceConfiguration</a>, <a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a>, <a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HttpSetServiceConfiguration</a>, and <a href="/windows/desktop/api/http/nf-http-httpupdateserviceconfiguration">HttpUpdateServiceConfiguration</a> functions when the <i>ConfigId</i> parameter is set to <b>HttpServiceConfigSslCcsCertInfo</b>.

## -see-also

<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_ccs_query">HTTP_SERVICE_CONFIG_SSL_CCS_QUERY</a>



<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_ccs_set">HTTP_SERVICE_CONFIG_SSL_CCS_SET</a>



<a href="/windows/desktop/api/http/nf-http-httpdeleteserviceconfiguration">HttpDeleteServiceConfiguration</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a>



<a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HttpSetServiceConfiguration</a>



<a href="/windows/desktop/api/http/nf-http-httpupdateserviceconfiguration">HttpUpdateServiceConfiguration</a>