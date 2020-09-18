---
UID: NS:http._HTTP_SERVICE_CONFIG_SSL_SNI_SET
title: HTTP_SERVICE_CONFIG_SSL_SNI_SET (http.h)
description: Used to add a new Secure Sockets Layer (SSL) Server Name Indication (SNI) certificate record to the SSL SNI store or retrieve an existing record from it.
helpviewer_keywords: ["*PHTTP_SERVICE_CONFIG_SSL_SNI_SET","HTTP_SERVICE_CONFIG_SSL_SNI_SET","HTTP_SERVICE_CONFIG_SSL_SNI_SET structure [HTTP]","PHTTP_SERVICE_CONFIG_SSL_SNI_SET","PHTTP_SERVICE_CONFIG_SSL_SNI_SET structure pointer [HTTP]","http.http_service_config_ssl_sni_set","http/HTTP_SERVICE_CONFIG_SSL_SNI_SET","http/PHTTP_SERVICE_CONFIG_SSL_SNI_SET"]
old-location: http\http_service_config_ssl_sni_set.htm
tech.root: http
ms.assetid: 382838B9-C15E-459F-AC40-ECA15EFC18B8
ms.date: 12/05/2018
ms.keywords: '*PHTTP_SERVICE_CONFIG_SSL_SNI_SET, HTTP_SERVICE_CONFIG_SSL_SNI_SET, HTTP_SERVICE_CONFIG_SSL_SNI_SET structure [HTTP], PHTTP_SERVICE_CONFIG_SSL_SNI_SET, PHTTP_SERVICE_CONFIG_SSL_SNI_SET structure pointer [HTTP], http.http_service_config_ssl_sni_set, http/HTTP_SERVICE_CONFIG_SSL_SNI_SET, http/PHTTP_SERVICE_CONFIG_SSL_SNI_SET'
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
req.typenames: HTTP_SERVICE_CONFIG_SSL_SNI_SET, *PHTTP_SERVICE_CONFIG_SSL_SNI_SET
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_SERVICE_CONFIG_SSL_SNI_SET
 - http/_HTTP_SERVICE_CONFIG_SSL_SNI_SET
 - PHTTP_SERVICE_CONFIG_SSL_SNI_SET
 - http/PHTTP_SERVICE_CONFIG_SSL_SNI_SET
 - HTTP_SERVICE_CONFIG_SSL_SNI_SET
 - http/HTTP_SERVICE_CONFIG_SSL_SNI_SET
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
 - HTTP_SERVICE_CONFIG_SSL_SNI_SET
---

# HTTP_SERVICE_CONFIG_SSL_SNI_SET structure


## -description

The 
<b>HTTP_SERVICE_CONFIG_SSL_SNI_SET</b> structure is used to add a new Secure Sockets Layer (SSL) Server Name Indication (SNI) certificate record to the SSL SNI store or retrieve an existing record from it. It is passed to the 
<a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HttpSetServiceConfiguration</a> function through the <i>pConfigInformation</i> parameter or to retrieve data from the 
<a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a> function through the <i>pOutputConfigInformation</i> parameter when the <i>ConfigId</i> parameter of either function is set to <b>HttpServiceConfigSslSniCertInfo</b>.

## -struct-fields

### -field KeyDesc

An <a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_sni_key">HTTP_SERVICE_CONFIG_SSL_SNI_KEY</a> structure that identifies the SSL SNI certificate record.

### -field ParamDesc

An <a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_param">HTTP_SERVICE_CONFIG_SSL_PARAM</a> structure that holds the contents of the specified SSL SNI certificate record.

## -see-also

<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_sni_key">HTTP_SERVICE_CONFIG_SSL_SNI_KEY</a>



<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_sni_query">HTTP_SERVICE_CONFIG_SSL_SNI_QUERY</a>



<a href="/windows/desktop/api/http/nf-http-httpdeleteserviceconfiguration">HttpDeleteServiceConfiguration</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a>



<a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HttpSetServiceConfiguration</a>