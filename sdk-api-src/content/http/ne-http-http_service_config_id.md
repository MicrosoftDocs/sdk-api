---
UID: NE:http._HTTP_SERVICE_CONFIG_ID
title: HTTP_SERVICE_CONFIG_ID (http.h)
description: Defines service configuration options.
helpviewer_keywords: ["*PHTTP_SERVICE_CONFIG_ID","HTTP_SERVICE_CONFIG_ID","HTTP_SERVICE_CONFIG_ID enumeration [HTTP]","HttpServiceConfigCache","HttpServiceConfigIPListenList","HttpServiceConfigMax","HttpServiceConfigSSLCertInfo","HttpServiceConfigSslCcsCertInfo","HttpServiceConfigSslSniCertInfo","HttpServiceConfigTimeout","HttpServiceConfigUrlAclInfo","PHTTP_SERVICE_CONFIG_ID","PHTTP_SERVICE_CONFIG_ID enumeration pointer [HTTP]","_http_http_service_config_id","http.http_service_config_id","http/HTTP_SERVICE_CONFIG_ID","http/HttpServiceConfigCache","http/HttpServiceConfigIPListenList","http/HttpServiceConfigMax","http/HttpServiceConfigSSLCertInfo","http/HttpServiceConfigSslCcsCertInfo","http/HttpServiceConfigSslSniCertInfo","http/HttpServiceConfigTimeout","http/HttpServiceConfigUrlAclInfo","http/PHTTP_SERVICE_CONFIG_ID"]
old-location: http\http_service_config_id.htm
tech.root: http
ms.assetid: 1b250408-4e3b-4cec-a31e-2c7f7ebad23b
ms.date: 12/05/2018
ms.keywords: '*PHTTP_SERVICE_CONFIG_ID, HTTP_SERVICE_CONFIG_ID, HTTP_SERVICE_CONFIG_ID enumeration [HTTP], HttpServiceConfigCache, HttpServiceConfigIPListenList, HttpServiceConfigMax, HttpServiceConfigSSLCertInfo, HttpServiceConfigSslCcsCertInfo, HttpServiceConfigSslSniCertInfo, HttpServiceConfigTimeout, HttpServiceConfigUrlAclInfo, PHTTP_SERVICE_CONFIG_ID, PHTTP_SERVICE_CONFIG_ID enumeration pointer [HTTP], _http_http_service_config_id, http.http_service_config_id, http/HTTP_SERVICE_CONFIG_ID, http/HttpServiceConfigCache, http/HttpServiceConfigIPListenList, http/HttpServiceConfigMax, http/HttpServiceConfigSSLCertInfo, http/HttpServiceConfigSslCcsCertInfo, http/HttpServiceConfigSslSniCertInfo, http/HttpServiceConfigTimeout, http/HttpServiceConfigUrlAclInfo, http/PHTTP_SERVICE_CONFIG_ID'
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
req.typenames: HTTP_SERVICE_CONFIG_ID, *PHTTP_SERVICE_CONFIG_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_SERVICE_CONFIG_ID
 - http/_HTTP_SERVICE_CONFIG_ID
 - PHTTP_SERVICE_CONFIG_ID
 - http/PHTTP_SERVICE_CONFIG_ID
 - HTTP_SERVICE_CONFIG_ID
 - http/HTTP_SERVICE_CONFIG_ID
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
 - HTTP_SERVICE_CONFIG_ID
---

# HTTP_SERVICE_CONFIG_ID enumeration


## -description

The 
<b>HTTP_SERVICE_CONFIG_ID</b> enumeration type defines service configuration options.

## -enum-fields

### -field HttpServiceConfigIPListenList

Specifies the IP Listen List used to register IP addresses on which to listen for SSL connections.

### -field HttpServiceConfigSSLCertInfo

Specifies the SSL certificate store.

<div class="alert"><b>Note</b>  If SSL is enabled in the HTTP Server API, TLS 1.0 may be used in place of SSL when the client application specifies TLS.</div>
<div> </div>

### -field HttpServiceConfigUrlAclInfo

Specifies the URL reservation store.

### -field HttpServiceConfigTimeout

Configures the HTTP Server API wide connection timeouts.


<div class="alert"><b>Note</b>  Windows Vista and later versions of Windows</div>
<div> </div>

### -field HttpServiceConfigCache

Used in the <a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a> and <a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HttpSetServiceConfiguration</a> functions.

<div class="alert"><b>Note</b>  Windows Server 2008 R2 and Windows 7 and later versions of Windows.</div>
<div> </div>

### -field HttpServiceConfigSslSniCertInfo

Specifies the SSL endpoint configuration with <i>Hostname:Port</i> as key. Used in the <a href="/windows/desktop/api/http/nf-http-httpdeleteserviceconfiguration">HttpDeleteServiceConfiguration</a>,  <a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a>, <a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HttpSetServiceConfiguration</a>, and <a href="/windows/desktop/api/http/nf-http-httpupdateserviceconfiguration">HttpUpdateServiceConfiguration</a> functions

<div class="alert"><b>Note</b>  Windows 8 and later versions of Windows.</div>
<div> </div>

### -field HttpServiceConfigSslCcsCertInfo

Specifies that an operation should be performed for the   SSL certificate record that specifies that Http.sys should consult the Centralized Certificate Store (CCS) store to find certificates if the port receives a Transport Layer Security (TLS) handshake.  Used in the <a href="/windows/desktop/api/http/nf-http-httpdeleteserviceconfiguration">HttpDeleteServiceConfiguration</a>,  <a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a>, <a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HttpSetServiceConfiguration</a>, and <a href="/windows/desktop/api/http/nf-http-httpupdateserviceconfiguration">HttpUpdateServiceConfiguration</a> functions

<div class="alert"><b>Note</b>  Windows 8 and later versions of Windows.</div>
<div> </div>

### -field HttpServiceConfigSetting

### -field HttpServiceConfigMax

Terminates the enumeration; is not used to define a service configuration option.

## -see-also

<a href="/windows/desktop/api/http/nf-http-httpdeleteserviceconfiguration">HttpDeleteServiceConfiguration</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a>



<a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HttpSetServiceConfiguration</a>



<a href="/windows/desktop/api/http/nf-http-httpupdateserviceconfiguration">HttpUpdateServiceConfiguration</a>