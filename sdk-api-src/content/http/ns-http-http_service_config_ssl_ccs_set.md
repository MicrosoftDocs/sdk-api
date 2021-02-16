---
UID: NS:http._HTTP_SERVICE_CONFIG_SSL_CCS_SET
title: HTTP_SERVICE_CONFIG_SSL_CCS_SET (http.h)
description: Represents the SSL certificate record that specifies that Http.sys should consult the Centralized Certificate Store (CCS) store to find certificates if the port receives a Transport Layer Security (TLS) handshake.
helpviewer_keywords: ["*PHTTP_SERVICE_CONFIG_SSL_CCS_SET","HTTP_SERVICE_CONFIG_SSL_CCS_SET","HTTP_SERVICE_CONFIG_SSL_CCS_SET structure [HTTP]","PHTTP_SERVICE_CONFIG_SSL_CCS_SET","PHTTP_SERVICE_CONFIG_SSL_CCS_SET structure pointer [HTTP]","http.http_service_config_ssl_ccs_set","http/HTTP_SERVICE_CONFIG_SSL_CCS_SET","http/PHTTP_SERVICE_CONFIG_SSL_CCS_SET"]
old-location: http\http_service_config_ssl_ccs_set.htm
tech.root: http
ms.assetid: BA815FB7-4A9F-4917-89E7-3CD108E1CEE3
ms.date: 12/05/2018
ms.keywords: '*PHTTP_SERVICE_CONFIG_SSL_CCS_SET, HTTP_SERVICE_CONFIG_SSL_CCS_SET, HTTP_SERVICE_CONFIG_SSL_CCS_SET structure [HTTP], PHTTP_SERVICE_CONFIG_SSL_CCS_SET, PHTTP_SERVICE_CONFIG_SSL_CCS_SET structure pointer [HTTP], http.http_service_config_ssl_ccs_set, http/HTTP_SERVICE_CONFIG_SSL_CCS_SET, http/PHTTP_SERVICE_CONFIG_SSL_CCS_SET'
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
req.typenames: HTTP_SERVICE_CONFIG_SSL_CCS_SET, *PHTTP_SERVICE_CONFIG_SSL_CCS_SET
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_SERVICE_CONFIG_SSL_CCS_SET
 - http/_HTTP_SERVICE_CONFIG_SSL_CCS_SET
 - PHTTP_SERVICE_CONFIG_SSL_CCS_SET
 - http/PHTTP_SERVICE_CONFIG_SSL_CCS_SET
 - HTTP_SERVICE_CONFIG_SSL_CCS_SET
 - http/HTTP_SERVICE_CONFIG_SSL_CCS_SET
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
 - HTTP_SERVICE_CONFIG_SSL_CCS_SET
---

# HTTP_SERVICE_CONFIG_SSL_CCS_SET structure


## -description

Represents the   SSL certificate record that specifies that Http.sys should consult the Centralized Certificate Store (CCS) store to find certificates if the port receives a Transport Layer Security (TLS) handshake.   Use this structure to add, delete, retrieve, or update that SSL certificate.

## -struct-fields

### -field KeyDesc

An <a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_ccs_key">HTTP_SERVICE_CONFIG_SSL_CCS_KEY</a> structure that identifies the SSL CCS certificate record.

### -field ParamDesc

An <a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_param">HTTP_SERVICE_CONFIG_SSL_PARAM</a> structure that holds the contents of the specified SSL CCS certificate record.

## -remarks

Pass this structure to the <a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HttpSetServiceConfiguration</a> or <a href="/windows/desktop/api/http/nf-http-httpdeleteserviceconfiguration">HttpDeleteServiceConfiguration</a> function through the <i>pConfigInformation</i> parameter to add or remove an SSL certificate record. Pass this structure to the <a href="/windows/desktop/api/http/nf-http-httpupdateserviceconfiguration">HttpUpdateServiceConfiguration</a> function through the <i>ConfigInfo</i> parameter to update an SSL certificate record.  Use  the <i>pOutputConfigInfo</i> parameter of the <a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a> function to retrieve SSL certificate record data in this structure. For all of these operations, set the <i>ConfigId</i> parameter of these functions to <b>HttpServiceConfigSslCcsCertInfo</b>.

## -see-also

<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_ccs_key">HTTP_SERVICE_CONFIG_SSL_CCS_KEY</a>



<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_param">HTTP_SERVICE_CONFIG_SSL_PARAM</a>



<a href="/windows/desktop/api/http/nf-http-httpdeleteserviceconfiguration">HttpDeleteServiceConfiguration</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a>



<a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HttpSetServiceConfiguration</a>



<a href="/windows/desktop/api/http/nf-http-httpupdateserviceconfiguration">HttpUpdateServiceConfiguration</a>