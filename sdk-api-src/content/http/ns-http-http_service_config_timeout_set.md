---
UID: NS:http._HTTP_SERVICE_CONFIG_TIMEOUT_SET
title: HTTP_SERVICE_CONFIG_TIMEOUT_SET (http.h)
description: Used to set the HTTP Server API wide timeout value.
helpviewer_keywords: ["*PHTTP_SERVICE_CONFIG_TIMEOUT_SET","*PHTTP_SERVICE_CONFIG_TIMEOUT_SET structure [HTTP]","HTTP_SERVICE_CONFIG_TIMEOUT_SET","HTTP_SERVICE_CONFIG_TIMEOUT_SET structure [HTTP]","http.http_service_config_timeout_set","http/*PHTTP_SERVICE_CONFIG_TIMEOUT_SET","http/HTTP_SERVICE_CONFIG_TIMEOUT_SET"]
old-location: http\http_service_config_timeout_set.htm
tech.root: http
ms.assetid: 928cb09d-9f63-4334-b034-ee27e950ce0a
ms.date: 12/05/2018
ms.keywords: '*PHTTP_SERVICE_CONFIG_TIMEOUT_SET, *PHTTP_SERVICE_CONFIG_TIMEOUT_SET structure [HTTP], HTTP_SERVICE_CONFIG_TIMEOUT_SET, HTTP_SERVICE_CONFIG_TIMEOUT_SET structure [HTTP], http.http_service_config_timeout_set, http/*PHTTP_SERVICE_CONFIG_TIMEOUT_SET, http/HTTP_SERVICE_CONFIG_TIMEOUT_SET'
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: HTTP_SERVICE_CONFIG_TIMEOUT_SET, *PHTTP_SERVICE_CONFIG_TIMEOUT_SET
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_SERVICE_CONFIG_TIMEOUT_SET
 - http/_HTTP_SERVICE_CONFIG_TIMEOUT_SET
 - PHTTP_SERVICE_CONFIG_TIMEOUT_SET
 - http/PHTTP_SERVICE_CONFIG_TIMEOUT_SET
 - HTTP_SERVICE_CONFIG_TIMEOUT_SET
 - http/HTTP_SERVICE_CONFIG_TIMEOUT_SET
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
 - HTTP_SERVICE_CONFIG_TIMEOUT_SET
---

# HTTP_SERVICE_CONFIG_TIMEOUT_SET structure


## -description

The <b>HTTP_SERVICE_CONFIG_TIMEOUT_SET</b> structure is used to set the HTTP Server API wide timeout value.

## -struct-fields

### -field KeyDesc

A member of the <a href="/windows/desktop/api/http/ne-http-http_service_config_timeout_key">HTTP_SERVICE_CONFIG_TIMEOUT_KEY</a> enumeration identifying the timer that is set.

### -field ParamDesc

The value, in seconds, for the timer. The value must be greater than zero.

## -remarks

An instance of the <b>HTTP_SERVICE_CONFIG_TIMEOUT_SET</b> structure is used to pass data in to the 
<a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HTTPSetServiceConfiguration</a> function through the <i>pConfigInformation</i> parameter or to retrieve data from the 
<a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HTTPQueryServiceConfiguration</a> function through the <i>pOutputConfigInformation</i> parameter when the <i>ConfigId</i> parameter of either function is equal to <b>HttpServiceConfigTimeout</b>.

Querying the existing value of an HTTP Server API wide timeout does not require administrative privileges. Setting the value, however, does require administrative privileges.

When the HTTP Server API wide timeout value is set with <a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HTTPSetServiceConfiguration</a>, the setting persists when the HTTP service is stopped and restarted.  The timeout value is applied to all the HTTP Server API applications on the machine.

The HTTP Server API timeout value is deleted by calling <a href="/windows/desktop/api/http/nf-http-httpdeleteserviceconfiguration">HTTPDeleteServiceConfiguration</a> with the <i>ConfigId</i> parameter set to <b>HttpServiceConfigTimeout</b> and the <i>pConfigInformation</i>  parameter pointing to the <b>HTTP_SERVICE_CONFIG_TIMEOUT_SET</b> structure. When a timer value is deleted, the persistent setting goes away, and HTTP Server API uses its hardcoded defaults.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-structures">HTTP Server API Version 2.0 Structures</a>



<a href="/windows/desktop/api/http/nf-http-httpdeleteserviceconfiguration">HTTPDeleteServiceConfiguration</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HTTPQueryServiceConfiguration</a>



<a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HTTPSetServiceConfiguration</a>