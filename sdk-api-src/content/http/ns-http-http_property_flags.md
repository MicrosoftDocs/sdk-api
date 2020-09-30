---
UID: NS:http._HTTP_PROPERTY_FLAGS
title: HTTP_PROPERTY_FLAGS (http.h)
description: Used by the property configuration structures to enable or disable a property on a configuration object when setting property configurations.
helpviewer_keywords: ["*PHTTP_PROPERTY_FLAGS","*PHTTP_PROPERTY_FLAGS structure [HTTP]","HTTP_PROPERTY_FLAGS","HTTP_PROPERTY_FLAGS structure [HTTP]","http.http_property_flags","http/*PHTTP_PROPERTY_FLAGS","http/HTTP_PROPERTY_FLAGS"]
old-location: http\http_property_flags.htm
tech.root: http
ms.assetid: cafa3b04-ac8b-4269-bfa9-fe8e9ab65936
ms.date: 12/05/2018
ms.keywords: '*PHTTP_PROPERTY_FLAGS, *PHTTP_PROPERTY_FLAGS structure [HTTP], HTTP_PROPERTY_FLAGS, HTTP_PROPERTY_FLAGS structure [HTTP], http.http_property_flags, http/*PHTTP_PROPERTY_FLAGS, http/HTTP_PROPERTY_FLAGS'
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
req.typenames: HTTP_PROPERTY_FLAGS, *PHTTP_PROPERTY_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_PROPERTY_FLAGS
 - http/_HTTP_PROPERTY_FLAGS
 - PHTTP_PROPERTY_FLAGS
 - http/PHTTP_PROPERTY_FLAGS
 - HTTP_PROPERTY_FLAGS
 - http/HTTP_PROPERTY_FLAGS
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
 - HTTP_PROPERTY_FLAGS
---

## -description

The <b>HTTP_PROPERTY_FLAGS</b> structure is used by the property configuration structures to enable or disable a property on a configuration object when setting property configurations.

When the configuration structure is used to query property configurations, this structure specifies whether the property is present on the configuration object.

## -struct-fields

### -field Present

The <b>Present</b> flag enables or disables a property, or determines whether the property is present on the configuration object.

A value of zero indicates the property is not present; a positive value indicates the property is present.

## -remarks

The property configuration structures are used in calls to <a href="/windows/desktop/api/http/nf-http-httpsetrequestqueueproperty">HttpSetRequestQueueProperty</a>, <a href="/windows/desktop/api/http/nf-http-httpsetserversessionproperty">HttpSetServerSessionProperty</a>, and <a href="/windows/desktop/api/http/nf-http-httpseturlgroupproperty">HttpSetUrlGroupProperty</a> to set properties on the corresponding configuration objects. The configuration structures are also used in calls to <a href="/windows/desktop/api/http/nf-http-httpqueryrequestqueueproperty">HttpQueryRequestQueueProperty</a>, <a href="/windows/desktop/api/http/nf-http-httpqueryserversessionproperty">HttpQueryServerSessionProperty</a>, and <a href="/windows/desktop/api/http/nf-http-httpqueryurlgroupproperty">HttpQueryUrlGroupProperty</a>,  to query properties on the corresponding configuration object. When properties are set on the URL Group, server session, or request queue, this structure enables or disables the property. When properties are queried for the URL Group, server session, or request queue, this structure is used by the application to determine if the property is present. For more information, see the list of property configuration structures in the See Also section below.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-structures">HTTP Server API Version 2.0 Structures</a>



<a href="/windows/desktop/api/http/ns-http-http_bandwidth_limit_info">HTTP_BANDWIDTH_LIMIT_INFO</a>



<a href="/windows/desktop/api/http/ns-http-http_binding_info">HTTP_BINDING_INFO</a>



<a href="/windows/desktop/api/http/ns-http-http_connection_limit_info">HTTP_CONNECTION_LIMIT_INFO</a>



<a href="/windows/desktop/api/http/ns-http-http_logging_info">HTTP_LOGGING_INFO</a>



<a href="/windows/desktop/api/http/ns-http-http_server_authentication_info">HTTP_SERVER_AUTHENTICATION_INFO</a>



<a href="/windows/desktop/api/http/ns-http-http_state_info">HTTP_STATE_INFO</a>



<a href="/windows/desktop/api/http/ns-http-http_timeout_limit_info">HTTP_TIMEOUT_LIMIT_INFO</a>