---
UID: NE:http._HTTP_SERVICE_CONFIG_TIMEOUT_KEY
title: HTTP_SERVICE_CONFIG_TIMEOUT_KEY (http.h)
description: The HTTP_SERVICE_CONFIG_TIMEOUT_KEY enumeration defines the type of timer that is queried or configured through the HTTP_SERVICE_CONFIG_TIMEOUT_SET structure.
helpviewer_keywords: ["*PHTTP_SERVICE_CONFIG_TIMEOUT_KEY","*PHTTP_SERVICE_CONFIG_TIMEOUT_KEY enumeration [HTTP]","HTTP_SERVICE_CONFIG_TIMEOUT_KEY","HTTP_SERVICE_CONFIG_TIMEOUT_KEY enumeration [HTTP]","HeaderWaitTimeout","IdleConnectionTimeout","http.http_service_config_timeout_key","http/*PHTTP_SERVICE_CONFIG_TIMEOUT_KEY","http/HTTP_SERVICE_CONFIG_TIMEOUT_KEY","http/HeaderWaitTimeout","http/IdleConnectionTimeout"]
old-location: http\http_service_config_timeout_key.htm
tech.root: http
ms.assetid: e591a6b8-e63f-40c3-bd48-e14cb9f89453
ms.date: 12/05/2018
ms.keywords: '*PHTTP_SERVICE_CONFIG_TIMEOUT_KEY, *PHTTP_SERVICE_CONFIG_TIMEOUT_KEY enumeration [HTTP], HTTP_SERVICE_CONFIG_TIMEOUT_KEY, HTTP_SERVICE_CONFIG_TIMEOUT_KEY enumeration [HTTP], HeaderWaitTimeout, IdleConnectionTimeout, http.http_service_config_timeout_key, http/*PHTTP_SERVICE_CONFIG_TIMEOUT_KEY, http/HTTP_SERVICE_CONFIG_TIMEOUT_KEY, http/HeaderWaitTimeout, http/IdleConnectionTimeout'
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
req.typenames: HTTP_SERVICE_CONFIG_TIMEOUT_KEY, *PHTTP_SERVICE_CONFIG_TIMEOUT_KEY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_SERVICE_CONFIG_TIMEOUT_KEY
 - http/_HTTP_SERVICE_CONFIG_TIMEOUT_KEY
 - PHTTP_SERVICE_CONFIG_TIMEOUT_KEY
 - http/PHTTP_SERVICE_CONFIG_TIMEOUT_KEY
 - HTTP_SERVICE_CONFIG_TIMEOUT_KEY
 - http/HTTP_SERVICE_CONFIG_TIMEOUT_KEY
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
 - HTTP_SERVICE_CONFIG_TIMEOUT_KEY
---

# HTTP_SERVICE_CONFIG_TIMEOUT_KEY enumeration


## -description

The <b>HTTP_SERVICE_CONFIG_TIMEOUT_KEY</b> enumeration defines the type of timer that is queried or configured through the <a href="/windows/desktop/api/http/ns-http-http_service_config_timeout_set">HTTP_SERVICE_CONFIG_TIMEOUT_SET</a> structure.

## -enum-fields

### -field IdleConnectionTimeout:0

The maximum time allowed for a connection to remain idle, after which, the connection is timed out and reset.

### -field HeaderWaitTimeout

The maximum time allowed to parse all the request headers, including the request line, after which, the connection is timed out and reset.

## -remarks

 The <b>HTTP_SERVICE_CONFIG_TIMEOUT_KEY</b> enumeration is used in the <a href="/windows/desktop/api/http/ns-http-http_service_config_timeout_set">HTTP_SERVICE_CONFIG_TIMEOUT_SET</a> structure to define the type of timer that is configured. The <b>HTTP_SERVICE_CONFIG_TIMEOUT_SET</b> structure passes data to  the <a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HTTPSetServiceConfiguration</a> function through  the <i>pConfigInformation</i> parameter or retrieves data from the 
<a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HTTPQueryServiceConfiguration</a> function through the <i>pOutputConfigInformation</i> parameter when the <i>ConfigId</i> parameter of either function is equal to <b>HttpServiceConfigTimeout</b>.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-enumeration-types">HTTP Server API Version 2.0 Enumeration Types</a>



<a href="/windows/desktop/api/http/ns-http-http_service_config_timeout_set">HTTP_SERVICE_CONFIG_TIMEOUT_SET</a>
