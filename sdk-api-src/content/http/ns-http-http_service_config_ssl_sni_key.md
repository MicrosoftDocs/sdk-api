---
UID: NS:http._HTTP_SERVICE_CONFIG_SSL_SNI_KEY
title: HTTP_SERVICE_CONFIG_SSL_SNI_KEY (http.h)
description: Serves as the key by which a given Secure Sockets Layer (SSL) Server Name Indication (SNI) certificate record is identified in the SSL SNI store.
helpviewer_keywords: ["*PHTTP_SERVICE_CONFIG_SSL_SNI_KEY","HTTP_SERVICE_CONFIG_SSL_SNI_KEY","HTTP_SERVICE_CONFIG_SSL_SNI_KEY structure [HTTP]","PHTTP_SERVICE_CONFIG_SSL_SNI_KEY","PHTTP_SERVICE_CONFIG_SSL_SNI_KEY structure pointer [HTTP]","http.http_service_config_ssl_sni_key","http/HTTP_SERVICE_CONFIG_SSL_SNI_KEY","http/PHTTP_SERVICE_CONFIG_SSL_SNI_KEY"]
old-location: http\http_service_config_ssl_sni_key.htm
tech.root: http
ms.assetid: 0EABB454-B4B9-4912-8E81-7930164B12F2
ms.date: 12/05/2018
ms.keywords: '*PHTTP_SERVICE_CONFIG_SSL_SNI_KEY, HTTP_SERVICE_CONFIG_SSL_SNI_KEY, HTTP_SERVICE_CONFIG_SSL_SNI_KEY structure [HTTP], PHTTP_SERVICE_CONFIG_SSL_SNI_KEY, PHTTP_SERVICE_CONFIG_SSL_SNI_KEY structure pointer [HTTP], http.http_service_config_ssl_sni_key, http/HTTP_SERVICE_CONFIG_SSL_SNI_KEY, http/PHTTP_SERVICE_CONFIG_SSL_SNI_KEY'
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
req.typenames: HTTP_SERVICE_CONFIG_SSL_SNI_KEY, *PHTTP_SERVICE_CONFIG_SSL_SNI_KEY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_SERVICE_CONFIG_SSL_SNI_KEY
 - http/_HTTP_SERVICE_CONFIG_SSL_SNI_KEY
 - PHTTP_SERVICE_CONFIG_SSL_SNI_KEY
 - http/PHTTP_SERVICE_CONFIG_SSL_SNI_KEY
 - HTTP_SERVICE_CONFIG_SSL_SNI_KEY
 - http/HTTP_SERVICE_CONFIG_SSL_SNI_KEY
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
 - HTTP_SERVICE_CONFIG_SSL_SNI_KEY
---

# HTTP_SERVICE_CONFIG_SSL_SNI_KEY structure


## -description

The 
<b>HTTP_SERVICE_CONFIG_SSL_SNI_KEY</b> structure serves as the key by which a given Secure Sockets Layer (SSL) Server Name Indication (SNI) certificate record is identified in the SSL SNI store.  It appears in the 
<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_sni_set">HTTP_SERVICE_CONFIG_SSL_SNI_SET</a> and the 
<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_sni_query">HTTP_SERVICE_CONFIG_SSL_SNI_QUERY</a> structures, and is passed as the <i>pConfigInformation</i> parameter to 
<a href="/windows/desktop/api/http/nf-http-httpdeleteserviceconfiguration">HttpDeleteServiceConfiguration</a>, 
<a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a>, and 
<a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HttpSetServiceConfiguration</a> when the <i>ConfigId</i> parameter is set to <b>HttpServiceConfigSslSniCertInfo</b>.

## -struct-fields

### -field IpPort

A <a href="/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)">SOCKADDR_STORAGE</a> structure that contains the Internet Protocol version 4 (IPv4) address with which this SSL SNI certificate is associated. It must be set to the IPv4 wildcard address of type <b>SOCKADDR_IN</b> with <b>ss_family</b> set to <b>AF_INET</b> and <b>sin_addr</b> filled with zeros. <b>Port</b> can be any valid port.

### -field Host

A pointer to a null-terminated Unicode UTF-16 string that represents the hostname.

## -see-also

<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_sni_query">HTTP_SERVICE_CONFIG_SSL_SNI_QUERY</a>



<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_sni_set">HTTP_SERVICE_CONFIG_SSL_SNI_SET</a>



<a href="/windows/desktop/api/http/nf-http-httpdeleteserviceconfiguration">HttpDeleteServiceConfiguration</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a>



<a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HttpSetServiceConfiguration</a>