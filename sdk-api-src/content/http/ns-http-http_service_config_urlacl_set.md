---
UID: NS:http._HTTP_SERVICE_CONFIG_URLACL_SET
title: HTTP_SERVICE_CONFIG_URLACL_SET (http.h)
description: Used to add a new record to the URL reservation store or retrieve an existing record from it.
helpviewer_keywords: ["*PHTTP_SERVICE_CONFIG_URLACL_SET","HTTP_SERVICE_CONFIG_URLACL_SET","HTTP_SERVICE_CONFIG_URLACL_SET structure [HTTP]","PHTTP_SERVICE_CONFIG_URLACL_SET","PHTTP_SERVICE_CONFIG_URLACL_SET structure pointer [HTTP]","_http_http_service_config_urlacl_set","http.http_service_config_urlacl_set","http/HTTP_SERVICE_CONFIG_URLACL_SET","http/PHTTP_SERVICE_CONFIG_URLACL_SET"]
old-location: http\http_service_config_urlacl_set.htm
tech.root: http
ms.assetid: 92fc3f65-0153-4075-a61b-48a63c8e0ffe
ms.date: 12/05/2018
ms.keywords: '*PHTTP_SERVICE_CONFIG_URLACL_SET, HTTP_SERVICE_CONFIG_URLACL_SET, HTTP_SERVICE_CONFIG_URLACL_SET structure [HTTP], PHTTP_SERVICE_CONFIG_URLACL_SET, PHTTP_SERVICE_CONFIG_URLACL_SET structure pointer [HTTP], _http_http_service_config_urlacl_set, http.http_service_config_urlacl_set, http/HTTP_SERVICE_CONFIG_URLACL_SET, http/PHTTP_SERVICE_CONFIG_URLACL_SET'
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
req.typenames: HTTP_SERVICE_CONFIG_URLACL_SET, *PHTTP_SERVICE_CONFIG_URLACL_SET
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_SERVICE_CONFIG_URLACL_SET
 - http/_HTTP_SERVICE_CONFIG_URLACL_SET
 - PHTTP_SERVICE_CONFIG_URLACL_SET
 - http/PHTTP_SERVICE_CONFIG_URLACL_SET
 - HTTP_SERVICE_CONFIG_URLACL_SET
 - http/HTTP_SERVICE_CONFIG_URLACL_SET
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
 - HTTP_SERVICE_CONFIG_URLACL_SET
---

# HTTP_SERVICE_CONFIG_URLACL_SET structure


## -description

The 
<b>HTTP_SERVICE_CONFIG_URLACL_SET</b> structure is used to add a new record to the URL reservation store or retrieve an existing record from it. An instance of the structure is used to pass data in through the <i>pConfigInformation</i> parameter of the 
<a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HTTPSetServiceConfiguration</a> function, or to retrieve data through the <i>pOutputConfigInformation</i> parameter of the 
<a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HTTPQueryServiceConfiguration</a> function when the <i>ConfigId</i> parameter of either function is equal to <b>HTTPServiceConfigUrlAclInfo</b>.

## -struct-fields

### -field KeyDesc

An 
<a href="/windows/desktop/api/http/ns-http-http_service_config_urlacl_key">HTTP_SERVICE_CONFIG_URLACL_KEY</a> structure that identifies the URL reservation record.

### -field ParamDesc

An 
<a href="/windows/desktop/api/http/ns-http-http_service_config_urlacl_param">HTTP_SERVICE_CONFIG_URLACL_PARAM</a> structure that holds the contents of the specified URL reservation record.

## -see-also

<a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HTTPQueryServiceConfiguration</a>



<a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HTTPSetServiceConfiguration</a>



<a href="/windows/desktop/api/http/ns-http-http_service_config_urlacl_key">HTTP_SERVICE_CONFIG_URLACL_KEY</a>



<a href="/windows/desktop/api/http/ns-http-http_service_config_urlacl_param">HTTP_SERVICE_CONFIG_URLACL_PARAM</a>